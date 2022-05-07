# 2022.05 1st Week Scrum

## INDEX
- Who am I?
- Scheule & Diary
-----
## Who am I?

##### *--안녕하세요. 전북대학교 소프트웨어공학과 20학번 김지희입니다. :>*
-----
## Schedule & Diary
### 2022.05.05
    5월 5일 어린이날.
    할머니 댁 갔다왔다.
    오랜만에 집에 와서 하루 죙일 먹으러 다녔다. 
    간만에 오빠랑 맥주 한잔해서 좋았다.
~~이런 시간 순삭이야..~~

### 2022.05.06
    오늘은 외할머니 뵀다.
    거제 케이블카, 바람의 언덕으로 놀러갔다왔다.
    재밌었지만 멀미해서 힘들어..

and..
- 소개프 보고서 제출

### 2022.05.07
    아침에 피부과가서 켈로이드 흉터치료하고 왔다.
and..
- 마프 보고서
- 모앱 <9장 그래픽과 이미지> 실습
    - 해당 코드는 이미지 블러링에 관한 코드이다.
        ```
        public class MainActivity extends AppCompatActivity {

        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(new MyGraphicView(this));
        }

        private static class MyGraphicView extends View {
            public MyGraphicView(Context context) {
                super(context);
            }

            @Override
            protected void onDraw(Canvas canvas){
                super.onDraw(canvas);
                Bitmap picture = BitmapFactory.decodeResource(getResources(), R.drawable.nyang);

                int picX = (this.getWidth() - picture.getWidth()) / 2;
                int picY = (this.getHeight() - picture.getHeight()) / 2;

                Paint paint = new Paint();
                BlurMaskFilter bMask;

                //BlurMaskFilter(반지름, 타입)
                bMask = new BlurMaskFilter(30, BlurMaskFilter.Blur.NORMAL);//NORMAL 타입
                paint.setMaskFilter(bMask);
                canvas.drawBitmap(picture, picX, picY, paint);
                picture.recycle();

            }
        }
        ```
- 모앱 조별 발표 준비 <10장 액티비티와 인텐트>
    - 실습 10-1 코드의 일부이다.
        ```
        public class MainActivity extends AppCompatActivity {

        @Override
        public void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);
            setTitle("메인 액티비티 (수정)");

            final RadioButton rdoSecond = findViewById(R.id.rdoSecond);

            Button btnNewActivity = (Button) findViewById(R.id.btnNewActivity);
            btnNewActivity.setOnClickListener(new View.OnClickListener() {
                public void onClick(View v) {
                    Intent intent;

                    if (rdoSecond.isChecked() == true)
                        intent = new Intent(getApplicationContext(), SecondActivity.class);
                    else
                        intent = new Intent(getApplicationContext(), ThirdActivity.class);

                    startActivity(intent);
                }
            });
        }
        ```
- AMPM GitHub Study 실습
    - Mark Down
        > 참고 자료
        > https://gist.github.com/ihoneymon/652be052a0727ad59601
