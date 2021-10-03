# mobillab4
1.Создадим проект, поместим изображения в папку res/drawable. Создадим в этой же папке файл rabbit_animation.xml
2.Добавим в созданный файл данный код:
    &lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
    &lt;animation-list xmlns:android=&quot;http://schemas.android.com/apk/res/android&quot;
    android:oneshot=&quot;false&quot; &gt;
    &lt;item android:drawable=&quot;@drawable/rabbit1&quot; android:duration=&quot;100&quot; /&gt;
    &lt;item android:drawable=&quot;@drawable/rabbit2&quot; android:duration=&quot;100&quot; /&gt;
    &lt;item android:drawable=&quot;@drawable/rabbit3&quot; android:duration=&quot;100&quot; /&gt;
    &lt;item android:drawable=&quot;@drawable/rabbit4&quot; android:duration=&quot;100&quot; /&gt;
    &lt;item android:drawable=&quot;@drawable/rabbit5&quot; android:duration=&quot;100&quot; /&gt;
    &lt;/animation-list&gt;
    
3.Поместим компонент ImageView.
4.Добавим запуск анимации:
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        ImageView img = findViewById(R.id.animationView);
        img.setBackgroundResource(R.drawable.rabbit_animation);
        AnimationDrawable frameAnimation = (AnimationDrawable) img.getBackground();
        frameAnimation.setOneShot(false);
        frameAnimation.start();
    }

    @Override
    protected void onStart() {
        super.onStart();
        AnimationDrawable img = (AnimationDrawable) findViewById(R.id.animationView).getBackground();

    }
