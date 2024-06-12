package application;
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.ColorPicker;
import javafx.scene.control.DatePicker;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class Main extends Application {

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        primaryStage.setTitle("Selector de Fecha y Color");


        DatePicker datePicker = new DatePicker();
        ColorPicker colorPicker = new ColorPicker();
        Button confirmButton = new Button("Confirmar");
        Label fechaLabel = new Label("Selecciona una fecha:");
        Label colorLabel = new Label("Selecciona un color:");


        confirmButton.setOnAction(e -> {
            System.out.println("Fecha seleccionada: " + datePicker.getValue());
            System.out.println("Color seleccionado: " + colorPicker.getValue());
        });


        VBox vbox = new VBox(10);
        vbox.getChildren().addAll(fechaLabel, datePicker, colorLabel, colorPicker, confirmButton);


        Scene scene = new Scene(vbox, 300, 200);
        primaryStage.setScene(scene);
        primaryStage.show();
    }
}
![image](https://github.com/stevenbetancourtuwu/stevennuwu/assets/172458170/c991ac84-8c98-405a-b9dc-0cd83b7aa7a7)
