# Java Swing Cheat Sheet



#### Window are very customizable, but below is a bare bones example to get going.  This should be placed in the constructor and an instance of your program should be created in the main function.
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

#### Components (to be cont..)
``` java
JButton button = new JButton(buttonString); // creates a clickable button with a label on it
JLabel label = new JLabel(labelString); // creates a label using a string
JList list = new JList(); // creates a list of items that are singularly selectable (see notes for use)
JTextArea ta = new JTextArea(); // creates multiple lines of plain text and allows the user to edit
JTextField tf = new JTextField(string); // creates a single line of text using the string and allows user to edit it
```

#### Notes
Populating a JList: JList have no methods to add or remove items.  A DefaultListModel object must be used, ex. below.
``` java
DefaultListModel<String> listModel = new DefaultListModel<String>();
JList list = new JList<String>(listModel);
listModel.add(index);
listModel.remove(index);
```

It is also important to note that unlike in here, variables should be declared outside your contructor and instanciated in the constructor.