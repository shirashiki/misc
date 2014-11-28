Android issues

http://stackoverflow.com/questions/19429948/couldnt-resolve-resource-in-android-studios-preview


ViewPager and fragments
http://stackoverflow.com/questions/18413309/how-to-implement-a-viewpager-with-different-fragments-layouts
http://stackoverflow.com/questions/17553374/android-app-fragments-vs-android-support-v4-app-using-viewpager

http://stackoverflow.com/questions/17295497/fragment-or-support-fragment


Game Development
http://www.kilobolt.com/game-development-tutorial.html

Off topic:
http://openbadges.org/


https://source.android.com/devices/sensors/index.html

Glossary
- HAL: hardware Abstraction Layer
- SoC: System on a chip






Sensor API
http://developer.android.com/reference/android/hardware/SensorManager.html

http://developer.android.com/reference/android/hardware/Sensor.html


Game Rotation vector
https://source.android.com/devices/sensors/sensor-types.html#game_rotation_vector


Motion & Android

Measuring movement with accelerometer and gyroscope
http://sfonge.com/forum/topic/measuring-movement-accelerometer-and-gyroscope

Compensating Accelerometer data with Gyro
http://sfonge.com/forum/topic/compensating-accelerometer-data-gyroscope

Example application for accelerometer/gyroscope processing on Android
http://sfonge.com/forum/topic/example-application-accelerometergyroscope-processing-android

Example application for accelerometer/compass processing on Android
http://sfonge.com/forum/topic/example-application-accelerometercompass-processing-android


http://developer.android.com/guide/topics/sensors/sensors_motion.html
https://source.android.com/devices/sensors/composite_sensors.html


Sensor Fusion
http://www.thousand-thoughts.com/2012/03/android-sensor-fusion-tutorial/
https://www.youtube.com/watch?v=C7JQ7Rpwn2k


Interesting Sensors:

Significant motion
Rotation vector



        startButton.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View v) {

                Intent myIntent = new Intent(MainActivity.this, SensorTestActivity.class);
                startActivity(myIntent);

            }
        });



