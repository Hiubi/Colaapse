# Colaapse
import javax.swing.*;


public class  MyFrame extends JFrame {


    MyFrame() {


        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300, 400);
        setResizable(true);
        setVisible(true);




        }
    }
import javax.swing.*;



public class MenuBar extends MyFrame {


    JMenu menu, submenu;
    JMenuItem i1, i2, i3, i4, i5;

     public MenuBar() {

        JMenuBar mb = new JMenuBar();
        menu = new JMenu("Menu");
        submenu = new JMenu("Sub Menu");
        i1 = new JMenuItem("Item 1");
        i2 = new JMenuItem("Item 2");
        i3 = new JMenuItem("Item 3");
        i4 = new JMenuItem("Item 4");
        i5 = new JMenuItem("Item 5");
        menu.add(i1);
        menu.add(i2);
        menu.add(i3);
        submenu.add(i4);
        submenu.add(i5);
        menu.add(submenu);
        mb.add(menu);
        mb.setVisible(true);


    }
}
import java.awt.EventQueue;

public class Test {
    public static void main(String[] args) {
        EventQueue.invokeLater(new Runnable() {
            @Override
            public void run() {
                new MyFrame();

            }
        });
    }
}
