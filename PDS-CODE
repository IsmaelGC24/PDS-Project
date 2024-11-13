import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class Main extends JPanel implements ActionListener {
    private JLabel lblWelcome;
    private JButton btnBuscarC;
    private JButton btnBuscarD;
    private JButton btnBuscarM;
    private JButton btnInfo;
    private JComboBox<String> buttonsBloques;
    private JLabel lblSelectLocation;
    private JButton btnColorsInfo;
    private JButton btnReciclaje;

    public Main() {
        String[] buttonsBloquesItems = {"Bloque 1", "Bloque 38", "Bloque 33", "Bloque 34", "Bloque 35", "Bloque 29", "Bloque 18", "Bloque 19", "Bloque 26", "Bloque 27"};

        lblWelcome = new JLabel("            ¡Bienvenido!");
        btnBuscarC = new JButton("Buscar Canecas");
        btnBuscarD = new JButton("Buscar Dispensadores");
        btnBuscarM = new JButton("Buscar Máquina");
        btnInfo = new JButton("Otra Información");
        buttonsBloques = new JComboBox<>(buttonsBloquesItems);
        lblSelectLocation = new JLabel("Selecciona Ubicación...");
        btnColorsInfo = new JButton("Colores de canecas");
        btnReciclaje = new JButton("Info Reciclaje");

        // actionListeners para los botones
        btnBuscarC.addActionListener(this);
        btnBuscarD.addActionListener(this);
        btnBuscarM.addActionListener(this);
        btnInfo.addActionListener(this);
        btnColorsInfo.addActionListener(this);
        btnReciclaje.addActionListener(this);

        setPreferredSize(new Dimension(800, 450));
        setLayout(null);

        add(lblWelcome);
        add(btnBuscarC);
        add(btnBuscarD);
        add(btnBuscarM);
        add(btnInfo);
        add(buttonsBloques);
        add(lblSelectLocation);
        add(btnColorsInfo);
        add(btnReciclaje);

        lblWelcome.setBounds(300, 0, 140, 55);
        btnBuscarC.setBounds(10, 380, 170, 45);
        btnBuscarD.setBounds(190, 380, 170, 45);
        btnBuscarM.setBounds(370, 380, 170, 45);
        buttonsBloques.setBounds(560, 85, 110, 25);
        lblSelectLocation.setBounds(560, 55, 200, 25);
        btnInfo.setBounds(560, 260, 190, 35);
        btnColorsInfo.setBounds(560, 175, 190, 40);
        btnReciclaje.setBounds(560, 220, 190, 35);
    } // end of constructor

    // manejador de los clics de los botones
    @Override
    public void actionPerformed(ActionEvent e) {
        String bloqueSeleccionado = (String) buttonsBloques.getSelectedItem();

        if (e.getSource() == btnBuscarC) {
            buscarCanecas(bloqueSeleccionado);
        } else if (e.getSource() == btnBuscarD) {
            buscarDispensadores(bloqueSeleccionado);
        } else if (e.getSource() == btnBuscarM) {
            buscarMaquinas(bloqueSeleccionado);
        } else if (e.getSource() == btnInfo) {
            mostrarOtraInformacion();
        } else if (e.getSource() == btnColorsInfo) {
            mostrarColoresCanecas();
        } else if (e.getSource() == btnReciclaje) {
            mostrarInfoReciclaje();
        }
    }// end of actionPerformed

    // Métodos para cada botón, con el bloque seleccionado
    private void buscarCanecas(String bloque) {
        String mensaje;
        switch (bloque) {
            case "Bloque 1":
                mensaje = "Las canecas más cercanas están en el tercer piso, al lado del ascensor.";
                break;
            case "Bloque 38":
                mensaje = "Canecas disponibles en el primer piso.";
                break;
            case "Bloque 33":
            case "Bloque 34":
            case "Bloque 35":
                mensaje = "Canecas disponibles en el pasillo de cada piso.";
                break;
            case "Bloque 29":
                mensaje = "Canecas disponibles en todos los pisos, excepto en la terraza.";
                break;
            case "Bloque 18":
                mensaje = "Canecas disponibles en cada piso al final del pasillo que da a los baños.";
                break;
            case "Bloque 19":
                mensaje = "Canecas disponibles en cada piso.";
                break;
            case "Bloque 26":
                mensaje = "Canecas disponibles saliendo a mano izquierda.";
                break;
            case "Bloque 27":
                mensaje = "Canecas disponibles saliendo por el primer piso, y en el Bloque 29 al lado del cajero.";
                break;
            default:
                mensaje = "Ubicación no especificada para canecas en " + bloque;
    }// end switch
        JOptionPane.showMessageDialog(this, mensaje);
    } // end buscarCanecas

    private void buscarDispensadores(String bloque) {
        String mensaje;
        switch (bloque) {
            case "Bloque 1":
                mensaje = "Dispensador disponible en el sexto piso.";
                break;
            case "Bloque 38":
                mensaje = "Dispensador disponible en el primer piso.";
                break;
            case "Bloque 33":
            case "Bloque 34":
            case "Bloque 35":
                mensaje = "Dispensador disponible en el primer piso.";
                break;
            case "Bloque 29":
                mensaje = "Dispensador más cercano en el Bloque 27, en la entrada.";
                break;
            case "Bloque 18":
            case "Bloque 19":
                mensaje = "Dispensador más cercano en la entrada del Bloque 26.";
                break;
            case "Bloque 26":
            case "Bloque 27":
                mensaje = "Dispensador disponible en la entrada del primer piso.";
                break;
            default:
                mensaje = "Ubicación no especificada para dispensadores en " + bloque;
    }// end switch
        JOptionPane.showMessageDialog(this, mensaje);
    } // end of buscarDispensadores

    private void buscarMaquinas(String bloque) {
        String mensaje = "La máquina de cupones solo está disponible en la cafetería";
        JOptionPane.showMessageDialog(this, mensaje);
    }

    private void mostrarOtraInformacion() {
        String mensaje = "Impacto ambiental de los residuos plásticos y beneficios de evitar productos envasados:\n\n" +
                         "1. *Impacto de los plásticos*: Los plásticos tardan cientos de años en descomponerse\n y liberan sustancias tóxicas al medio ambiente. Cada vez que usamos plásticos \n de un solo uso, contribuimos a la contaminación de océanos y suelos, \n afectando la vida de muchas especies.\n\n" +
                         "2. *Beneficios de tomar agua*: Al elegir agua de fuentes sostenibles en lugar de \n bebidas envasadas, reducimos el uso de plásticos y el consumo de productos \n que requieren grandes cantidades de energía para su producción. \n Tomar agua es una opción saludable y eco-amigable.";
        JOptionPane.showMessageDialog(this, mensaje);
    }

    private void mostrarColoresCanecas() {
        String mensaje = "*Caneca Negra*: Residuos no reciclables, como empaques de comida, \n papel higiénico, servilletas usadas y otros residuos orgánicos contaminados.\n\n" +
                         "*Caneca Blanca*: Materiales reciclables limpios, como papel, cartón, plásticos \n (botellas, envases), y metales (latas de aluminio y envases metálicos).\n\n" +
                         "*Caneca Verde*: Residuos orgánicos, como restos de comida, cáscaras de frutas y \n verduras, plantas y otros residuos biodegradables.";
        JOptionPane.showMessageDialog(this, mensaje);
    }

    private void mostrarInfoReciclaje() {
        String mensaje = "El reciclaje es fundamental para reducir el impacto ambiental de \n nuestros residuos. Por eso en la universidad, debemos promoverlo \n para disminuir la cantidad de desechos enviados a rellenos sanitarios, \n conservando así los espacio limpios y fomentando un ambiente \n bueno para todos.";
        JOptionPane.showMessageDialog(this, mensaje);
    }

    public static void main(String[] args) {
        JFrame frame = new JFrame("MyPanel");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.getContentPane().add(new Main());
        frame.pack();
        frame.setVisible(true);
      
} // end of psvm
} // end of Class
