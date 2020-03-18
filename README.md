# BuildingAnEmojiDictionaryApp
Building an Emoji Dictionary App

# Table Views
1. [Anatomy of a TableView](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#1-anatomy-of-a-tableview)
2. [TableView Style](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#2-tableview-style)
3. [TableView Editing](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#3-tableview-editing)
4. [TableView Cells](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#4-tableview-cells)
5. [TableView Readibility Margings](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#5-tableview-readibility-margings)
6. [Index Paths](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#6-index-paths)
7. [Arrays and TableViews](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#7-arrays-and-tableviews)
8. [Cell Dequeueing](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#8-cell-dequeueing)
9. [TableView Protocols](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#9-tableview-protocols)
10. [TableView DataSource](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#10-tableview-datasource)
11. [Number of sections](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#11-number-of-sections)
12. [Number of rows in a section](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#12-number-of-rows-in-a-section)
13. [Cell for Row at Index Path](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#13-cell-for-row-at-index-path)
14. [Implement the data soruce](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#14-implement-the-data-soruce)
15. [Table View Delegate](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#15-table-view-delegate)
16. [Accesory Button Tapped for Row](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#16-accesory-button-tapped-for-row)
17. [Did Select Row](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#17-did-select-row)
18. [Implement the delegate](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#18-implement-the-delegate)
19. [Reorder cells](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#19-reorder-cells)
20. [Reload Data](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#20-reload-data)

# Intermediate Table Views

21. [Custom Table Views](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#21-custom-table-views)
22. [Content Hugging](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#22-content-hugging)
23. [Create Cell Subclass](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#23-create-cell-subclass)
24. [Edit Table Views](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#24-edit-table-views)
25. [Delete Items](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#25-delete-items)
26. [Add and Edid Emoji](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#26-add-and-edid-emoji)
27. [Static Table Views](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#27-static-table-views)
28. [Enable Emoji Keyboard](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#28-enable-emoji-keyboard)
29. [Pass Data to Static Table View](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#29-pass-data-to-static-table-view)
30. [Add Action Button with unwind Segue](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#30-add-action-button-with-unwind-segue)
31. [Update Save BUtton](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#31-update-save-button)
32. [Save Emoji](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#32-save-emoji)
33. [Automatic Row Height](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#33-automatic-row-height)
34. [Compression Resistence](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#34-compression-resistence)


<p align="left">
<img src="https://github.com/carlos-santiago-2017/BuildingAnEmojiDictionaryApp/blob/master/1.png">
</p>

# Table Views
# [1. Anatomy of a TableView](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [2. TableView Style](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [3. TableView Editing](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [4. TableView Cells](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [5. TableView Readibility Margings](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [6. Index Paths](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [7. Arrays and TableViews](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [8. Cell Dequeueing](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [9. TableView Protocols](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [10. TableView DataSource](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [11. Number of sections](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [12. Number of rows in a section](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [13. Cell for Row at Index Path](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [14. Implement the data soruce](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [15. Table View Delegate](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [16. Accesory Button Tapped for Row](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [17. Did Select Row](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [18. Implement the delegate](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [19. Reorder cells](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [20. Reload Data](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# 
# Intermediate Table Views
# 
# [21. Custom Table Views](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [22. Content Hugging](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [23. Create Cell Subclass](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [24. Edit Table Views](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [25. Delete Items](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [26. Add and Edid Emoji](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [27. Static Table Views](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [28. Enable Emoji Keyboard](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [29. Pass Data to Static Table View](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [30. Add Action Button with unwind Segue](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [31. Update Save BUtton](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [32. Save Emoji](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [33. Automatic Row Height](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)
# [34. Compression Resistence](https://github.com/c4arl0s/BuildingAnEmojiDictionaryApp#buildinganemojidictionaryapp)

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




