# EasyLottoReload

ซอฟแวร์จองหวยเสรี

https://www.lotto.ktbnetbank.com/KTBLotto/#/login


public class MainActivity extends AppCompatActivity {
   TextView tvNum;
   int i = 0;
   @Override
   protected void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);
       setContentView(R.layout.activity_main);

       tvNum = (TextView) findViewById(R.id.tvNum);

       Thread thread  = new Thread() {
           @Override
           public void run() {
               while( i<5 ) {
                   try {
                       Thread.sleep(1000);
                       System.out.println(i++);
                       //openBrowser(View v)
                   handler.sendEmptyMessage(0);
                   } catch (InterruptedException e) {
                       e.printStackTrace();
                   }
               }
           }
       };

protected void openBrowser(View v) {
   String url = "https://www.lotto.ktbnetbank.com/KTBLotto/#/login";
   Intent browserIntent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
   startActivity(browserIntent);
}
