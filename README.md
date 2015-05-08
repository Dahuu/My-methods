package com.huakadg1.bit.thirdparty;

import android.support.v7.app.ActionBarActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.view.View;
import android.widget.ImageView;

import com.skyfishjy.library.RippleBackground;


public class MainActivity extends ActionBarActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState)

    {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        final RippleBackground rippleBackground=(RippleBackground)findViewById(R.id.content);

        ImageView imageView=(ImageView)findViewById(R.id.centerImage);
        imageView.setOnClickListener(new View.OnClickListener()
        {
            @Override
            public void onClick(View view)
            {
                //creating a toggle
                if (rippleBackground.isRippleAnimationRunning())
                {
                   rippleBackground.stopRippleAnimation();
                }
                else
                {
                    rippleBackground.startRippleAnimation();
                }


            }
        });

    }


}
