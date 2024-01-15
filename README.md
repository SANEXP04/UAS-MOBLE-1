 # UAS PEMROGRAMAN MOBILE 1

Nama: Ihsan Hadimulya<br>
Kelas : TI.22.A.1<br>
NIM: 312210047<br>
Matkul : Pemrograman Mobile 1<br>
Dosen : Donny Maulana, S.Kom., M.M.S.I.

<h3>Assalamualaikum Wr.Wb disini saya akan menampilkan hasil akhir project atau Project UAS ,serta menampilkan codingan yang berfungsi untuk menampilkan Fragment serta menammpilkan video yang didalamnya ada kode youtube di dalam Fragment java nya serta memasukan gambar dengan fungsi imagebutton berikut adalah hasilnya dan juga ada beberapa project sebelumnnya</h3>

  
## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Helloworld|[Click Here](#helloworld)|
|2|Count|[Click Here](#count)|
|3|Sianida|[Click Here](#sianidaproject)|
|4|twoactivity|[Click Here](#twoactivity)|
|5|FragmentActivity|[Click Here](#fragment)|
|6|Secondfragment|[Click Here](#secondfragment)|
|7|Firstfragment|[Click Here](#firstfragment)|
|8|Fragment3|[Click Here](#fragment3)|
|8|Hasil Run AKhir|[Click Here](#Hasil-Run-Semua-Project)|




## helloworld


><h3> Java Hello World</h3>

    package com.intent;
    
    import android.os.Bundle;
    import androidx.appcompat.app.AppCompatActivity;
    
    public class HelloActivity extends AppCompatActivity {
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_hello);
        }
    }

<h2>disini hasil run nya https://github.com/lampubohlam/intent_mobile-V2.git </h2>

><h3> XML Hello World</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".HelloActivity">

    <ImageView
        android:id="@+id/background"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@drawable/bg_hello"
        android:adjustViewBounds="true"
        android:scaleType="centerCrop"/>

    <TextView
        android:id="@+id/Texthello"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="courier"
        android:gravity="center"
        android:text="@string/hello_text"
        android:textColor="@color/yellow"
        android:textSize="11pt"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:ignore="TextSizeCheck" />

    </androidx.constraintlayout.widget.ConstraintLayout>

## count


<h3> Berikut kodingan project count/bilangan Fibonacci JAVA dan XML nya</h3>

><h3> Java Count/Fibonacci</h3>
    package com.intent;

    import android.annotation.SuppressLint;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.TextView;
    import android.widget.Toast;
    
    import androidx.appcompat.app.AppCompatActivity;
    
    
    public class CountActivity extends AppCompatActivity {
        private int nCount = 0;

        private TextView nShowCount;
    
        @SuppressLint("MissingInflatedId")
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_count);
            nShowCount = findViewById(R.id.show_count);
        }
    
        public void showToast(View view){
            Toast toast = Toast.makeText(this, "Menghitung Bilangan",
                    Toast.LENGTH_SHORT);
            toast.show();
        }
    
        @SuppressLint("SetTextI18n")
        public void countUp(View view){
            nCount++;
            if (nShowCount != null)
                nShowCount.setText(Integer.toString(nCount));
        }
    }


  > <h3>XML Count/Fibonacci</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".CountActivity">
    
        <ImageView
            android:id="@+id/background"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:background="@drawable/bg_count"
            android:adjustViewBounds="true"
            android:scaleType="centerCrop" />
    
        <Button
            android:id="@+id/button_toast"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginEnd="8dp"
            android:layout_marginStart="8dp"
            android:layout_marginTop="8dp"
            android:background="@color/colorPrimary"
            android:onClick="showToast"
            android:text="@string/button_label_toast"
            android:textColor="@android:color/white"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            tools:ignore="UsingOnClickInXml"/>
    
        <Button
            android:id="@+id/button_count"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginEnd="8dp"
            android:layout_marginStart="8dp"
            android:layout_marginBottom="8dp"
            android:background="@color/colorPrimary"
            android:onClick="countUp"
            android:text="@string/button_label_count"
            android:textColor="@android:color/white"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintBottom_toBottomOf="parent"
            tools:ignore="UsingOnClickInXml" />
    
        <TextView
            android:id="@+id/show_count"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginEnd="8dp"
            android:text="@string/count_initial_value"
            android:textAlignment="center"
            android:textColor="@color/blue"
            android:textSize="160sp"
            android:textStyle="bold"
            app:layout_constraintBottom_toTopOf="@+id/button_count"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/button_toast"
            tools:ignore="RtlCompat" />
    
    </androidx.constraintlayout.widget.ConstraintLayout>
> <h3> Hasil Run di link https://github.com/lampubohlam/Bilangan-fibonance_UTS.git </h3>


## sianida project

> <h3>Java Sianida</h3>

    package com.intent;
    import android.os.Bundle;
    import androidx.appcompat.app.AppCompatActivity;
    
    public class SianidaActivity extends AppCompatActivity {
        @Override
        protected void onCreate(Bundle savedInstanceState){
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_sianida);
        }
    }


> <h3>XML Sianida</h3>
          
    <?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        xmlns:tools="http://schemas.android.com/tools"
        tools:context=".SianidaActivity">
    
        <TextView
            android:id="@+id/article_heading"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:background="@color/colorPrimary"
            android:padding="@dimen/padding_regular"
            android:text="@string/article_title"
            android:textAppearance="@android:style/TextAppearance.DeviceDefault.Large"
            android:textColor="@android:color/white"
            android:textStyle="bold" />
    
        <ScrollView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@id/article_heading">
    
            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical">
    
                <TextView
                    android:id="@+id/article_subheading"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:padding="@dimen/padding_regular"
                    android:text="@string/article_subtitle"
                    android:textAlignment="center"
                    android:textAppearance="@android:style/TextAppearance.DeviceDefault"
                    android:textColor="#8D6E63" />
    
                <TextView
                    android:id="@+id/article"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:autoLink="web"
                    android:lineSpacingExtra="@dimen/line_spacing"
                    android:padding="@dimen/padding_regular"
                    android:text="@string/article_teks"
                    tools:ignore="VisualLintLongText" />
            </LinearLayout>
        </ScrollView>
    </RelativeLayout>
 > hasil run ada di link berikut : https://github.com/lampubohlam/intent_mobile-V2.git

## twoactivity

> <h3>Java Twoactivity</h3>

    package com.intent;
    
    import androidx.appcompat.app.AppCompatActivity;
    import android.content.Intent;
    import android.os.Bundle;
    import android.util.Log;
    import android.view.View;
    import android.widget.EditText;
    import android.widget.TextView;
    
    public class TwoactActivity extends AppCompatActivity {
    
        private static final String LOG_TAG = TwoactActivity.class.getSimpleName();
        public static final String EXTRA_MESSAGE = "com.example.android.Twoact2Activity.extra.MESSAGE";
        public static final int TEXT_REQUEST = 1;
        private EditText mMessageEditText;
        private TextView mReplyHeadTextView;
        private TextView mReplyTextView;
      
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_twoact);
      
            mMessageEditText = findViewById(R.id.editText_main);
            mReplyHeadTextView = findViewById(R.id.text_header_reply);
            mReplyTextView = findViewById(R.id.text_message_reply);
        }
      
        public void LaunchSecondActivity(View view) {
            Log.d(LOG_TAG, "Button clicked!");
            Intent intent = new Intent(this, Twoact2Activity.class);
            String message = mMessageEditText.getText().toString();
            intent.putExtra(EXTRA_MESSAGE, message);
            startActivityForResult(intent, TEXT_REQUEST);
        }
      
        @Override
        public void onActivityResult(int requestCode, int resultCode, Intent data) {
            super.onActivityResult(requestCode, resultCode, data);
      
            if (resultCode == TEXT_REQUEST) {
                if (resultCode == RESULT_OK) {
                    String reply = data.getStringExtra(Twoact2Activity.EXTRA_REPLY);
      
                    mReplyHeadTextView.setVisibility(View.VISIBLE);
      
                    mReplyHeadTextView.setText(reply);
                    mReplyHeadTextView.setVisibility(View.VISIBLE);
                }
            }
        }
      }
      
> <h3>Java Twoactivity 2</h3>

    package com.intent;
    
    import android.content.Intent;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.EditText;
    import android.widget.TextView;
    import androidx.appcompat.app.AppCompatActivity;
    
    public class Twoact2Activity extends AppCompatActivity {
        public static final String EXTRA_REPLY ="com.example.android.Twoact2Activity.extra.REPLY";
        private EditText mReply;
    
        @Override
        protected void onCreate(Bundle savedInstanceState){
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_twoact2);
            mReply = findViewById(R.id.editText_second);
            Intent intent = getIntent();
            String message = intent.getStringExtra(TwoactActivity.EXTRA_MESSAGE);
            TextView textView = findViewById(R.id.text_message);
            textView.setText(message);
        }
        public void returnReply(View view){
            String reply = mReply.getText().toString();
            Intent replyIntent = new Intent();
            setResult(RESULT_OK, replyIntent);
            finish();
        }
    }
    
> <h3>Layout Twoactivity</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        tools:context=".TwoactActivity">
    
        <ImageView
            android:id="@+id/background"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:adjustViewBounds="true"
            android:scaleType="centerCrop"
            android:src="@drawable/bg_twoact1" />
    
        <TextView
            android:id="@+id/text_header_reply"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginLeft="8dp"
            android:layout_marginTop="16dp"
            android:text="@string/text_header_reply"
            android:textAppearance="@style/TextAppearance.AppCompat.Medium"
            android:textStyle="bold"
            android:visibility="invisible"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"/>
    
        <TextView
            android:id="@+id/text_message_reply"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginLeft="8dp"
            android:layout_marginTop="8dp"
            android:visibility="invisible"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/text_header_reply" />
    
        <Button
            android:id="@+id/button_main"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            android:layout_marginRight="16dp"
            android:text="@string/button_main"
            android:onClick="LaunchSecondActivity"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintRight_toRightOf="parent"
            tools:ignore="UsingOnClickInXml"/>
    
        <EditText
            android:id="@+id/editText_main"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginEnd="8dp"
            android:layout_marginBottom="16dp"
            android:ems="10"
            android:hint="@string/editText_main"
            android:inputType="textLongMessage"
            android:minHeight="48dp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toStartOf="@+id/button_main"
            app:layout_constraintStart_toStartOf="parent" />
    </androidx.constraintlayout.widget.ConstraintLayout>

> <h3>Layout Twoactivity 2</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        tools:context=".Twoact2Activity">
    
        <ImageView
            android:id="@+id/background"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:adjustViewBounds="true"
            android:scaleType="centerCrop"
            android:src="@drawable/bg_twoact1" />
    
        <TextView
            android:id="@+id/text_header"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginLeft="8dp"
            android:layout_marginTop="16dp"
            android:text="@string/text_header"
            android:textAppearance="@style/TextAppearance.AppCompat.Medium"
            android:textStyle="bold"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent" />
    
        <TextView
            android:id="@+id/text_message"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginLeft="8dp"
            android:layout_marginTop="8dp"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/text_header" />
    
        <Button
            android:id="@+id/button_second"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            android:layout_marginRight="16dp"
            android:text="@string/button_second"
            android:onClick="returnReply"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintRight_toRightOf="parent"
            tools:ignore="UsingOnClickInXml" />
    
        <EditText
            android:id="@+id/editText_second"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginEnd="8dp"
            android:layout_marginBottom="16dp"
            android:ems="10"
            android:hint="@string/editText_second"
            android:inputType="textLongMessage"
            android:minHeight="48dp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toStartOf="@+id/button_second"
            app:layout_constraintStart_toStartOf="parent" />
    </androidx.constraintlayout.widget.ConstraintLayout>

> <h3>Hasil run Ada Di link berikut https://github.com/lampubohlam/intent_mobile-V2.git </h3>


<h2> Masuk ke Fragment</h2>

> <h3>Langkah pertama tambahkan kode berikut di build.gradle.kts(Modul:app)</h3>

    implementation("androidx.fragment:fragment:$fragment_version")
    implementation("com.pierfrancescosoffritti.androidyoutubeplayer:core:11.0.1")

<h3>Lalu lanjut ke tahap selanjutnya membuat Fragment Atau tampilan depan nya silahkan ikuti langkah semua dibawah dengan membuat JAVA dan FIle XML nya dan jangn lupa masukan src Image nya </h3>

## fragment

> <h3>Java FragmentActivity</h3>

    package com.intent;
    
    import android.os.Bundle;
    import androidx.annotation.Nullable;
    import androidx.appcompat.app.AppCompatActivity;
    import com.google.android.material.tabs.TabLayout;
    
    public class FragmentActivity extends AppCompatActivity {
    
        @Override
        protected void onCreate(@Nullable Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_fragment);
            getSupportFragmentManager().beginTransaction()
                    .replace(R.id.framelayout, new FirstFragment())
                    .commit();
    
            TabLayout tabLayout = findViewById(R.id.tablayout);
            tabLayout.addOnTabSelectedListener(new TabLayout.OnTabSelectedListener() {
                @Override
                public void onTabSelected(TabLayout.Tab tab) {
                    switch (tab.getPosition()) {
                        case 0:
                            getSupportFragmentManager().beginTransaction()
                                    .replace(R.id.framelayout, new FirstFragment())
                                    .commit();
                            break;
                        case 1:
                            getSupportFragmentManager().beginTransaction()
                                    .replace(R.id.framelayout, new SecondFragment())
                                    .commit();
                            break;
                        case 2:
                            getSupportFragmentManager().beginTransaction()
                                    .replace(R.id.framelayout, new ThirdFragment())
                                    .commit();
                            break;
                    }
                }
    
                @Override
                public void onTabUnselected(TabLayout.Tab tab) {}
    
                @Override
                public void onTabReselected(TabLayout.Tab tab) {}
            });
        }
    }

> <h3>Layout Activity fragment</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:orientation="vertical"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".FragmentActivity">
    
        <TextView
            android:id="@+id/header"
            android:layout_width="match_parent"
            android:layout_height="60dp"
            android:background="#004685"
            android:paddingStart="8dp"
            android:paddingTop="8dp"
            android:text="@string/movies"
            android:textColor="#FFFFFF"
            android:textSize="24sp"
            android:textStyle="bold"
            android:gravity="center"
            tools:ignore="RtlSymmetry" />
    
        <com.google.android.material.tabs.TabLayout
            android:id="@+id/tablayout"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:background="#000000"
            app:tabIndicator="@color/white"
            app:tabSelectedTextColor="@color/white">
    
            <com.google.android.material.tabs.TabItem
                android:id="@+id/tab1"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="@string/horror"
                />
    
            <com.google.android.material.tabs.TabItem
                android:id="@+id/tab2"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="@string/action"
                />
    
            <com.google.android.material.tabs.TabItem
                android:id="@+id/tab3"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="@string/romance"
                />
    
        </com.google.android.material.tabs.TabLayout>
    
    
        <FrameLayout
            android:id="@+id/framelayout"
            android:layout_width="match_parent"
            android:layout_height="match_parent" />
    
    </LinearLayout>
                  
## firstfragment

> <h3>Java FirstFragtment</h3>
                   
    package com.intent;
    
    import android.os.Bundle;
    import android.view.KeyEvent;
    import android.view.LayoutInflater;
    import android.view.View;
    import android.view.ViewGroup;
    import android.widget.ImageButton;
    import androidx.fragment.app.Fragment;
    import com.pierfrancescosoffritti.androidyoutubeplayer.core.player.YouTubePlayer;
    import com.pierfrancescosoffritti.androidyoutubeplayer.core.player.views.YouTubePlayerView;
    
    public class FirstFragment extends Fragment {
        private static final String YOUTUBE_VIDEO_ID_1 = "iTOaFootkSk";
        private static final String YOUTUBE_VIDEO_ID_2 = "s1xjv2iCQUc";
        private static final String YOUTUBE_VIDEO_ID_3 = "o_kTUnzp5ng";
        private YouTubePlayerView youTubePlayerView;
        private YouTubePlayer youTubePlayer;
        private boolean isVideoOpen = false;
    
        public FirstFragment() {
            // Required empty public constructor
        }
    
        @Override
        public View onCreateView(LayoutInflater inflater, ViewGroup container,
                                 Bundle savedInstanceState) {
            // Inflate the layout for this fragment
            View view = inflater.inflate(R.layout.fragment_first, container, false);
    
            // Initialize YouTube Player View
            youTubePlayerView = view.findViewById(R.id.youtube_player_view);
            getLifecycle().addObserver(youTubePlayerView);
    
            // Set up ImageButton click listeners
            ImageButton imageButton1 = view.findViewById(R.id.image1);
            imageButton1.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_1));
    
            ImageButton imageButton2 = view.findViewById(R.id.image2);
            imageButton2.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_2));
    
            ImageButton imageButton3 = view.findViewById(R.id.image3);
            imageButton3.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_3));
    
            // Set up KeyEvent callback for handling back button
            view.setFocusableInTouchMode(true);
            view.requestFocus();
            view.setOnKeyListener((v, keyCode, event) -> {
                if (keyCode == KeyEvent.KEYCODE_BACK && event.getAction() == KeyEvent.ACTION_UP) {
                    // Check if YouTubePlayerView is visible and handle back button
                    if (isVideoOpen) {
                        closeVideo();
                        return true;  // consume the back button event
                    }
                }
                return false;  // do not consume the back button event
            });
    
            return view;
        }
    
        private void loadVideo(String videoId) {
            // Show the YouTubePlayerView
            youTubePlayerView.setVisibility(View.VISIBLE);
    
            // Load and play the YouTube video
            youTubePlayerView.getYouTubePlayerWhenReady(youTubePlayer -> {
                if (youTubePlayer != null) {
                    youTubePlayer.loadVideo(videoId, 0);
                    this.youTubePlayer = youTubePlayer;
                    isVideoOpen = true;
                }
            });
        }
    
        private void closeVideo() {
            // Hide the YouTubePlayerView
            youTubePlayerView.setVisibility(View.GONE);
    
            // Release resources associated with the YouTubePlayerView
            if (youTubePlayer != null) {
                youTubePlayer.pause();
                youTubePlayer.cueVideo("", 0);
                isVideoOpen = false;
            }
        }
    }
    
> <h3>Layout fragment_first</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@color/backgroundall"
        tools:context=".FirstFragment">
    
        <ImageButton
            android:id="@+id/image1"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="8dp"
            android:scaleType="centerInside"
            android:src="@drawable/horror"
            android:background="@color/backgroundfilm"
            android:onClick="loadVideo1"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title1"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image1"
            android:layout_marginStart="16dp"
            android:layout_marginTop="8dp"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/Horror1"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating1"
            android:layout_toRightOf="@id/image1"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title1"
            android:textColor="@color/grey"
            android:text="@string/ratinga1"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis1"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating1"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image1"
            android:maxLines="4"
            android:text="@string/sinopsish1"
            android:textColor="@color/black" />
    
        <ImageButton
            android:id="@+id/image2"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="15dp"
            android:layout_below="@+id/image1"
            android:scaleType="centerInside"
            android:onClick="loadVideo2"
            android:background="@color/backgroundfilm"
            android:src="@drawable/horror2"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title2"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image2"
            android:layout_marginStart="16dp"
            android:layout_marginTop="12dp"
            android:layout_below="@id/sinopsis1"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/Horror2"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating2"
            android:layout_toRightOf="@id/image2"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title2"
            android:textColor="@color/grey"
            android:text="@string/ratinga2"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis2"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating2"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image2"
            android:maxLines="4"
            android:text="@string/sinopsish2"
            android:textColor="@color/black" />
    
        <ImageButton
            android:id="@+id/image3"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="15dp"
            android:layout_below="@+id/image2"
            android:scaleType="centerInside"
            android:background="@color/backgroundfilm"
            android:onClick="loadVideo3"
            android:src="@drawable/horror3"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title3"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image3"
            android:layout_marginStart="16dp"
            android:layout_marginTop="12dp"
            android:layout_below="@id/sinopsis2"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/Horror3"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating3"
            android:layout_toRightOf="@id/image3"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title3"
            android:textColor="@color/grey"
            android:text="@string/ratinga3"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis3"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating3"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image3"
            android:maxLines="4"
            android:text="@string/sinopsish3"
            android:textColor="@color/black" />
    
        <com.pierfrancescosoffritti.androidyoutubeplayer.core.player.views.YouTubePlayerView
            android:id="@+id/youtube_player_view"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_centerInParent="true"
            android:visibility="gone" />
    
    </RelativeLayout>                      


## secondfragment

carilah video dari youtube dan salin pada link dibelakanngnya contoh dalam gambar ini
 ![image](https://github.com/lampubohlam/UAS_MOBILE_SM3/assets/116137169/5629d0ed-38ab-4d4b-8cb3-445ce2cb5fed)

Salin lah link yang ditandai garis biru dibelakang =

> <h3>Java SecondFragment</h3>

    package com.intent;
    
    import android.os.Bundle;
    import android.view.KeyEvent;
    import android.view.LayoutInflater;
    import android.view.View;
    import android.view.ViewGroup;
    import android.widget.ImageButton;
    import androidx.fragment.app.Fragment;
    import com.pierfrancescosoffritti.androidyoutubeplayer.core.player.YouTubePlayer;
    import com.pierfrancescosoffritti.androidyoutubeplayer.core.player.views.YouTubePlayerView;
    
    public class SecondFragment extends Fragment {
        private static final String YOUTUBE_VIDEO_ID_1 = "itnqEauWQZM";
        private static final String YOUTUBE_VIDEO_ID_2 = "odM92ap8_c0";
        private static final String YOUTUBE_VIDEO_ID_3 = "TcMBFSGVi1c";
        private YouTubePlayerView youTubePlayerView;
        private YouTubePlayer youTubePlayer;
        private boolean isVideoOpen = false;
    
        public SecondFragment() {
            // Required empty public constructor
        }
    
        @Override
        public View onCreateView(LayoutInflater inflater, ViewGroup container,
                                 Bundle savedInstanceState) {
            // Inflate the layout for this fragment
            View view = inflater.inflate(R.layout.fragment_second, container, false);
    
            // Initialize YouTube Player View
            youTubePlayerView = view.findViewById(R.id.youtube_player_view);
            getLifecycle().addObserver(youTubePlayerView);
    
            // Set up ImageButton click listeners
            ImageButton imageButton1 = view.findViewById(R.id.image1);
            imageButton1.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_1));
    
            ImageButton imageButton2 = view.findViewById(R.id.image2);
            imageButton2.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_2));
    
            ImageButton imageButton3 = view.findViewById(R.id.image3);
            imageButton3.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_3));
    
            // Set up KeyEvent callback for handling back button
            view.setFocusableInTouchMode(true);
            view.requestFocus();
            view.setOnKeyListener((v, keyCode, event) -> {
                if (keyCode == KeyEvent.KEYCODE_BACK && event.getAction() == KeyEvent.ACTION_UP) {
                    // Check if YouTubePlayerView is visible and handle back button
                    if (isVideoOpen) {
                        closeVideo();
                        return true;  // consume the back button event
                    }
                }
                return false;  // do not consume the back button event
            });
    
            return view;
        }
    
        private void loadVideo(String videoId) {
            // Show the YouTubePlayerView
            youTubePlayerView.setVisibility(View.VISIBLE);
    
            // Load and play the YouTube video
            youTubePlayerView.getYouTubePlayerWhenReady(youTubePlayer -> {
                if (youTubePlayer != null) {
                    youTubePlayer.loadVideo(videoId, 0);
                    this.youTubePlayer = youTubePlayer;
                    isVideoOpen = true;
                }
            });
        }
    
        private void closeVideo() {
            // Hide the YouTubePlayerView
            youTubePlayerView.setVisibility(View.GONE);
    
            // Release resources associated with the YouTubePlayerView
            if (youTubePlayer != null) {
                youTubePlayer.pause();
                youTubePlayer.cueVideo("", 0);
                isVideoOpen = false;
            }
        }
    }

> <h3>Layout fragment_second</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@color/backgroundall"
        tools:context=".SecondFragment">
    
        <ImageButton
            android:id="@+id/image1"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="8dp"
            android:scaleType="centerInside"
            android:src="@drawable/action"
            android:background="@color/backgroundfilm"
            android:onClick="loadVideo1"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title1"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image1"
            android:layout_marginStart="16dp"
            android:layout_marginTop="8dp"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/action1"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating1"
            android:layout_toRightOf="@id/image1"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title1"
            android:textColor="@color/grey"
            android:text="@string/ratingc1"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis1"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating1"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image1"
            android:maxLines="4"
            android:text="@string/sinopsisa1"
            android:textColor="@color/black" />
    
        <ImageButton
            android:id="@+id/image2"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="15dp"
            android:layout_below="@+id/image1"
            android:scaleType="centerInside"
            android:onClick="loadVideo2"
            android:background="@color/backgroundfilm"
            android:src="@drawable/action2"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title2"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image2"
            android:layout_marginStart="16dp"
            android:layout_marginTop="11dp"
            android:layout_below="@id/sinopsis1"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/action2"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating2"
            android:layout_toRightOf="@id/image2"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title2"
            android:textColor="@color/grey"
            android:text="@string/ratingc2"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis2"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating2"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image2"
            android:maxLines="4"
            android:text="@string/sinopsisa2"
            android:textColor="@color/black" />
    
        <ImageButton
            android:id="@+id/image3"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="15dp"
            android:layout_below="@+id/image2"
            android:scaleType="centerInside"
            android:background="@color/backgroundfilm"
            android:onClick="loadVideo3"
            android:src="@drawable/action3"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title3"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image3"
            android:layout_marginStart="16dp"
            android:layout_marginTop="11dp"
            android:layout_below="@id/sinopsis2"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/action3"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating3"
            android:layout_toRightOf="@id/image3"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title3"
            android:textColor="@color/grey"
            android:text="@string/ratingc3"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis3"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating3"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image3"
            android:maxLines="4"
            android:text="@string/sinopsisa3"
            android:textColor="@color/black" />
    
        <com.pierfrancescosoffritti.androidyoutubeplayer.core.player.views.YouTubePlayerView
            android:id="@+id/youtube_player_view"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_centerInParent="true"
            android:visibility="gone" />
    
    </RelativeLayout>

                      
## fragment3

> <h3>Java ThirdFragment</h3>

    package com.intent;
    
    import android.os.Bundle;
    import android.view.KeyEvent;
    import android.view.LayoutInflater;
    import android.view.View;
    import android.view.ViewGroup;
    import android.widget.ImageButton;
    import androidx.fragment.app.Fragment;
    import com.pierfrancescosoffritti.androidyoutubeplayer.core.player.YouTubePlayer;
    import com.pierfrancescosoffritti.androidyoutubeplayer.core.player.views.YouTubePlayerView;
    
    public class ThirdFragment extends Fragment {
        private static final String YOUTUBE_VIDEO_ID_1 = "p7lKOU5w3Mg";
        private static final String YOUTUBE_VIDEO_ID_2 = "X_b-wNkz4DU";
        private static final String YOUTUBE_VIDEO_ID_3 = "b0NS7FP1loU";
        private YouTubePlayerView youTubePlayerView;
        private YouTubePlayer youTubePlayer;
        private boolean isVideoOpen = false;
    
        public ThirdFragment() {
            // Required empty public constructor
        }
    
        @Override
        public View onCreateView(LayoutInflater inflater, ViewGroup container,
                                 Bundle savedInstanceState) {
            // Inflate the layout for this fragment
            View view = inflater.inflate(R.layout.fragment_third, container, false);
    
            // Initialize YouTube Player View
            youTubePlayerView = view.findViewById(R.id.youtube_player_view);
            getLifecycle().addObserver(youTubePlayerView);
    
            // Set up ImageButton click listeners
            ImageButton imageButton1 = view.findViewById(R.id.image1);
            imageButton1.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_1));
    
            ImageButton imageButton2 = view.findViewById(R.id.image2);
            imageButton2.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_2));
    
            ImageButton imageButton3 = view.findViewById(R.id.image3);
            imageButton3.setOnClickListener(v -> loadVideo(YOUTUBE_VIDEO_ID_3));
    
            // Set up KeyEvent callback for handling back button
            view.setFocusableInTouchMode(true);
            view.requestFocus();
            view.setOnKeyListener((v, keyCode, event) -> {
                if (keyCode == KeyEvent.KEYCODE_BACK && event.getAction() == KeyEvent.ACTION_UP) {
                    // Check if YouTubePlayerView is visible and handle back button
                    if (isVideoOpen) {
                        closeVideo();
                        return true;  // consume the back button event
                    }
                }
                return false;  // do not consume the back button event
            });
    
            return view;
        }
    
        private void loadVideo(String videoId) {
            // Show the YouTubePlayerView
            youTubePlayerView.setVisibility(View.VISIBLE);
    
            // Load and play the YouTube video
            youTubePlayerView.getYouTubePlayerWhenReady(youTubePlayer -> {
                if (youTubePlayer != null) {
                    youTubePlayer.loadVideo(videoId, 0);
                    this.youTubePlayer = youTubePlayer;
                    isVideoOpen = true;
                }
            });
        }
    
        private void closeVideo() {
            // Hide the YouTubePlayerView
            youTubePlayerView.setVisibility(View.GONE);
    
            // Release resources associated with the YouTubePlayerView
            if (youTubePlayer != null) {
                youTubePlayer.pause();
                youTubePlayer.cueVideo("", 0);
                isVideoOpen = false;
            }
        }
    }

> <h3>Layout fragment_third</h3>

    <?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@color/backgroundall"
        tools:context=".SecondFragment">
    
        <ImageButton
            android:id="@+id/image1"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="8dp"
            android:scaleType="centerInside"
            android:src="@drawable/romance"
            android:background="@color/backgroundfilm"
            android:onClick="loadVideo1"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title1"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image1"
            android:layout_marginStart="16dp"
            android:layout_marginTop="8dp"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/romance1"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating1"
            android:layout_toRightOf="@id/image1"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title1"
            android:textColor="@color/grey"
            android:text="@string/ratingr1"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis1"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating1"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image1"
            android:maxLines="4"
            android:text="@string/sinopsisr1"
            android:textColor="@color/black" />
    
        <ImageButton
            android:id="@+id/image2"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="15dp"
            android:layout_below="@+id/image1"
            android:scaleType="centerInside"
            android:onClick="loadVideo2"
            android:background="@color/backgroundfilm"
            android:src="@drawable/romance2"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title2"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image2"
            android:layout_marginStart="16dp"
            android:layout_marginTop="11dp"
            android:layout_below="@id/sinopsis1"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/romance2"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating2"
            android:layout_toRightOf="@id/image2"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title2"
            android:textColor="@color/grey"
            android:text="@string/ratingr2"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis2"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating2"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image2"
            android:maxLines="4"
            android:text="@string/sinopsisr2"
            android:textColor="@color/black" />
    
        <ImageButton
            android:id="@+id/image3"
            android:layout_width="150dp"
            android:layout_height="145dp"
            android:layout_marginTop="15dp"
            android:layout_below="@+id/image2"
            android:scaleType="centerInside"
            android:background="@color/backgroundfilm"
            android:onClick="loadVideo3"
            android:src="@drawable/romance3"
            tools:ignore="SpeakableTextPresentCheck" />
    
        <TextView
            android:id="@+id/title3"
            android:layout_width="180dp"
            android:layout_height="41dp"
            android:layout_toRightOf="@id/image3"
            android:layout_marginStart="16dp"
            android:layout_marginTop="11dp"
            android:layout_below="@id/sinopsis2"
            android:textSize="18sp"
            android:textStyle="bold"
            android:text="@string/romance3"
            android:textColor="@color/black"/>
    
        <TextView
            android:id="@+id/rating3"
            android:layout_toRightOf="@id/image3"
            android:layout_width="180dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="16dp"
            android:layout_marginTop="4dp"
            android:layout_below="@id/title3"
            android:textColor="@color/grey"
            android:text="@string/ratingr3"
            android:textSize="14sp"
            android:textStyle="bold"/>
    
        <TextView
            android:id="@+id/sinopsis3"
            android:layout_width="match_parent"
            android:layout_height="80dp"
            android:layout_below="@id/rating3"
            android:layout_marginStart="16dp"
            android:layout_marginLeft="14dp"
            android:layout_marginTop="5dp"
            android:layout_toRightOf="@id/image3"
            android:maxLines="4"
            android:text="@string/sinopsisr3"
            android:textColor="@color/black" />
    
        <com.pierfrancescosoffritti.androidyoutubeplayer.core.player.views.YouTubePlayerView
            android:id="@+id/youtube_player_view"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_centerInParent="true"
            android:visibility="gone" />
    
    </RelativeLayout>


## Hasil-Run-Semua-Project

https://github.com/SANEXP04/UAS-MOBLE-1/assets/115678077/c8a18d74-33a5-465e-954a-a3f88e24b206

