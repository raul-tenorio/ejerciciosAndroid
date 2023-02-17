
# Ejercicio_39
## Evento Touch : DIbujar un circulo

Una actividad fundamental es poder detectar cuando el usuario selecciona o toca la pantalla táctil.

Problema:
Desarrollar un programa que dibuje un círculo en la coordenada 100,100. Cuando se presione otra parte de la pantalla táctil proceder a trasladar el círculo a dicha coordenada.

1 - Creamos un proyecto llamado: Proyecto039
Borramos el TextView que agrega automáticamente el Android Studio y definimos el id del ConstraintLayout con el valor: layout1:
Confeccionar un programa para administrar un calendario de actividades diarias. Los nombres de archivos corresponderán a las fechas que ingresamos. Luego cuando consultamos una fecha verificamos si hay un archivo de texto que coincida con dicha fecha.

1) El diseño visual de la aplicación sera la siguiente <br>
![image](https://i.ibb.co/cc9G152/Screenshot-20230216-235838.png)

2) La configuración del touch en el mainactivity es:<br>
<code>public class MainActivity extends AppCompatActivity implements View.OnTouchListener{

    private int corx, cory;
    private Lienzo fondo;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        corx = 100;
        cory = 100;
        ConstraintLayout layout1 = findViewById(R.id.layout1);
        fondo = new Lienzo(this);
        fondo.setOnTouchListener(this);
        layout1.addView(fondo);
    }

    public boolean onTouch(View v, MotionEvent event) {
        corx = (int) event.getX();
        cory = (int) event.getY();
        fondo.invalidate();
        return true;
    }

    class Lienzo extends View {

        public Lienzo(Context context) {
            super(context);
        }

        protected void onDraw(Canvas canvas) {
            canvas.drawRGB(255, 255, 0);
            Paint pincel1 = new Paint();
            pincel1.setARGB(255, 255, 0, 0);
            pincel1.setStrokeWidth(4);
            pincel1.setStyle(Paint.Style.STROKE);
            canvas.drawCircle(corx, cory, 20, pincel1);
        }
    }
}</code>
  
3) Definimos losa tributos las coordenadas donde se va dibujar el circulo.
<code> private int corx, cory;
    private Lienzo fondo; </code>
    
4) En el metodo oncreate inicializamos los atributos.
<code>corx = 100;
        cory = 100;
        ConstraintLayout layout1 = findViewById(R.id.layout1);
        fondo = new Lienzo(this);
        fondo.setOnTouchListener(this);
        layout1.addView(fondo);</code>
        
6) El metodo onDrwa pintal el fondo amarillo.
<code> protected void onDraw(Canvas canvas) {
            canvas.drawRGB(255, 255, 0);
            Paint pincel1 = new Paint();
            pincel1.setARGB(255, 255, 0, 0);
            pincel1.setStrokeWidth(4);
            pincel1.setStyle(Paint.Style.STROKE);
            canvas.drawCircle(corx, cory, 20, pincel1);
        } </code>
        
8)
<b>La interfaz visual en tiempo de ejecución</b><br>
<img src="https://i.ibb.co/rs3Fqg3/Whats-App-Image-2023-02-17-at-00-04-01-2.jpg" alt="drawing" width="200"/>
<img src="https://i.ibb.co/tYFCCSS/Whats-App-Image-2023-02-17-at-00-04-01-1.jpg" alt="drawing" width="200"/>
<img src="https://i.ibb.co/TMdntQc/Whats-App-Image-2023-02-17-at-00-04-01.jpg" alt="drawing" width="200"/>

