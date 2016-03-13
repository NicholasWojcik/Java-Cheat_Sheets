# Java Swing Cheat Sheet

## Setting Up Your Window In Your Programs Constructor (make sure an instance is made in the main method)

> Window are very customizable, but below is a bare bones example to get going
``` java
 JFrame window = new JFrame(windowTitleString);
 window.setSize(xLength, yLength);
 window.setFocusable(true);
 window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
 window.setResizable(false);
 window.setLayout(null) //allows you to set the exact location of your following components
 
 //create component(s)
 Button button = new Button("My App");
 button.setBounds(xCoor, yCoor, xLength, yLength);
 
 //add your components here, ex. using the button created above
 window.getContentPane().add(button);
 
 //set your component visable, this should always come after the components you want to be visable
 window.setVisable(true);
```

## Components (to be cont..)
* **JButton** _button_ = new **JButton**(_buttonString_); ---- creates a clickable button with a label on it
* **JLabel** _label_ = new **JLabel**(_labelString_); ------------ creates a label using a string
* **JList** _list_ = new **JList**(); ---------------------------------- creates a list of items that are singularly selectable (see notes for use)
* **JTextArea** _ta_ = new **JTextArea**(); -------------------- creates multiple lines of plain text and allows the user to edit
* **JTextField** _tf_ = new **JTextField**(_string_); ------------- creates a single line of text using the string and allows user to edit it

## Notes
> Populating a JList: JList have no methods to add or remove items.  A DefaultListModel object must be used, ex. below.
* **DefaultListModel**<_String_> _listModel_ = new **DefaultListModel**<_String_>();
* **JList** _list_ = new **JList**<String>(_listModel_);
* _listModel_.add(index);
* _listModel_.remove(index);
> 
> It is also important to note that unlike in here, variables should be declared outside your contructor and
> instanciated in the constructor.