# Java Swing Cheat Sheet

## Setting Up Your Window In Your Programs Constructor (make sure an instance is made in the main method)
> Window are very customizable, but below is a bare bones example to get going
* **JFrame** _window_ = new **JFrame**(_windowTitleString_);
* _window_.setSize(_xLength_, _yLength_);
* _window_.setFocusable(_true_);
* _window_.setDefaultCloseOperation(_JFrame_.EXIT_ON_CLOSE);
* _window_.setResizable(_false_);
* _window_.setLayout(_null_) //allows you to set the exact location of your following components
*
* //create component(s)
* **Button** _button_ = new **Button**(_"My App"_);
* **_button_.setBounds(_xCoor_, _yCoor_, _xLength_, _yLength_);
* 
* //add your components here, ex. using the button created above
* _window_.getContentPane().add(_button_);
* 
* //set your component visable, this should always come after the components you want to be visable
* _window_.setVisable(_true_);

## Components (to be cont..)
* **Button** _button_ = new **Button**(_buttonString_); ---- creates a clickable button with a label on it
* **Label** _label_ = new **Label**(_labelString_); ------------ creates a label using a string
* **List** _list_ = new **List**(); ---------------------------------- creates a list of items that are singularly selectable (see notes for populating)
* **TextArea** _ta_ = new **TextArea**(); -------------------- creates multiple lines of plain text and allows the user to edit
* **TextField** _tf_ = new **TextField**(_string_); ------------- creates a single line of text using the string and allows the user to edit it
