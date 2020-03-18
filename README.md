# BuildingAnEmojiDictionaryApp
Building an Emoji Dictionary App

# Table Views
1. [Anatomy of a TableView]()
2. [TableView Style]()
3. [TableView Editing]()
4. [TableView Cells]()
5. [TableView Readibility Margings]()
6. [Index Paths]()
7. [Arrays and TableViews]()
8. [Cell Dequeueing]()
9. [TableView Protocols]()
10. [TableView DataSource]()
11. [Number of sections]()
12. [Number of rows in a section]()
13. [Cell for Row at Index Path]()
14. [Implement the data soruce]()
15. [Table View Delegate]()
16. [Accesory Button Tapped for Row]()
17. [Did Select Row]()
18. [Implement the delegate]()
19. [Reorder cells]()
20. [Reload Data]()

# Intermediate Table Views

21. [Custom Table Views]()
22. [Content Hugging]()
23. [Create Cell Subclass]()
24. [Edit Table Views]()
25. [Delete Items]()
26. [Add and Edid Emoji]()
27. [Static Table Views]()
28. [Enable Emoji Keyboard]()
29. [Pass Data to Static Table View]()
30. [Add Action Button with unwind Segue]()
31. [Update Save BUtton]()
32. [Save Emoji]()
33. [Automatic Row Height]()
34. [Compression Resistence]()


<p align="left">
<img src="https://github.com/carlos-santiago-2017/BuildingAnEmojiDictionaryApp/blob/master/1.png">
</p>

# Table Views
# 1. [Anatomy of a TableView]()
# 2. [TableView Style]()
# 3. [TableView Editing]()
# 4. [TableView Cells]()
# 5. [TableView Readibility Margings]()
# 6. [Index Paths]()
# 7. [Arrays and TableViews]()
# 8. [Cell Dequeueing]()
# 9. [TableView Protocols]()
# 10. [TableView DataSource]()
# 11. [Number of sections]()
# 12. [Number of rows in a section]()
# 13. [Cell for Row at Index Path]()
# 14. [Implement the data soruce]()
# 15. [Table View Delegate]()
# 16. [Accesory Button Tapped for Row]()
# 17. [Did Select Row]()
# 18. [Implement the delegate]()
# 19. [Reorder cells]()
# 20. [Reload Data]()
# 
# Intermediate Table Views
# 
# 21. [Custom Table Views]()
# 22. [Content Hugging]()
# 23. [Create Cell Subclass]()
# 24. [Edit Table Views]()
# 25. [Delete Items]()
# 26. [Add and Edid Emoji]()
# 27. [Static Table Views]()
# 28. [Enable Emoji Keyboard]()
# 29. [Pass Data to Static Table View]()
# 30. [Add Action Button with unwind Segue]()
# 31. [Update Save BUtton]()
# 32. [Save Emoji]()
# 33. [Automatic Row Height]()
# 34. [Compression Resistence]()

# EmojiTableViewController.swift

``` swift
//
//  EmojiTableViewController.swift
//  BuildingAnEmojiDictionaryApp
//
//  Created by Carlos Santiago Cruz on 06/09/18.
//  Copyright © 2018 Carlos Santiago Cruz. All rights reserved.
//

import UIKit

class EmojiTableViewController: UITableViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
         navigationItem.leftBarButtonItem = editButtonItem
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    // MARK: - Table view data source
    
    override func numberOfSections(in tableView: UITableView) -> Int {
        return 1
    }

    override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        if section == 0 {
            return emojis.count
        } else {
            return 0
        }
    }
    override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = tableView.dequeueReusableCell(withIdentifier: "Emojicell" , for: indexPath)
        let emoji = emojis[indexPath.row]
        cell.showsReorderControl = true
        cell.textLabel?.text = "\(emoji.symbol) -\(emoji.name)"
        cell.detailTextLabel?.text = emoji.description
        
        return cell
    }
    override func tableView(_ tableView: UITableView, didSelectRowAt indexPath: IndexPath) {
        let emoji = emojis[indexPath.row]
        print("\(emoji.symbol) \(indexPath)")
    }
    override func tableView(_ tableView: UITableView, moveRowAt sourceIndexPath: IndexPath, to destinationIndexPath: IndexPath) {
        let movedEmoji = emojis.remove(at: sourceIndexPath.row)
        emojis.insert(movedEmoji, at: destinationIndexPath.row)
        tableView.reloadData()
    }
    @IBAction func editButtonTapped(_ sender: UIBarButtonItem) {
        let tableViewEditingMode = tableView.isEditing
        tableView.setEditing(!tableViewEditingMode, animated: true)
    }
    
}

```

# Emoji.swift

``` swift
//
//  Emoji.swift
//  BuildingAnEmojiDictionaryApp
//
//  Created by Carlos Santiago Cruz on 06/09/18.
//  Copyright © 2018 Carlos Santiago Cruz. All rights reserved.
//
import Foundation
import UIKit
// class Emoji which model de object
class Emoji {
    var symbol: String
    var name: String
    var description: String
    var usage: String
    init(symbol: String, name: String, description: String, usage: String){
        self.symbol = symbol
        self.name = name
        self.description = description
        self.usage = usage
    }
}
// emojis is an array of Emoji type
    var emojis: [Emoji] = [
        Emoji(symbol: "😀", name: "Grinning Face", description: "A typical smiley face.", usage: "happiness"),
        Emoji(symbol: "😕", name: "Confused Face", description: "A confused, puzzled face.", usage: "unsurwhat to think; displeasure"),
        Emoji(symbol: "😍", name: "Heart Eyes", description: "A smiley face with hearts for eyes.", usage: "love of something; attractive"), Emoji(symbol: "👮", name: "Police Officer", description: "A police officer wearing a blue cap with a gold badge.", usage: "person of authority"),
        Emoji(symbol: "🐢", name: "Turtle", description: "A cute turtle.", usage: "Something slow"),
        Emoji(symbol: "🐘", name: "Elephant", description: "A gray elephant.", usage: "good memory"),
        Emoji(symbol: "🍝", name: "Spaghetti",description: "A plate of spaghetti.", usage: "spaghetti"),
        Emoji(symbol: "🎲", name: "Die", description: "A single die.", usage: "taking a risk, chance; game"),
        Emoji(symbol: "⛺️", name: "Tent", description: "A small tent.", usage: "camping"),
        Emoji(symbol: "📚", name: "Stack of Books", description: "Three colored books stacked on each other.", usage: "homework, studying"),
        Emoji(symbol: "💔", name: "Broken Heart", description: "A red, broken heart.", usage: "extreme sadness"), Emoji(symbol: "💤", name: "Snore", description: "Three blue \'z\'s.", usage: "tired, sleepiness"),
        Emoji(symbol: "🏁", name: "Checkered Flag", description: "A black-and-white checkered flag.", usage: "completion"),
        Emoji(symbol: "👊", name: "puño", description: "es un puño", usage: "se usa para 'golpear'")
]
```




