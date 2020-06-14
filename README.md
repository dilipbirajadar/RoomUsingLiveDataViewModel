
# RoomUsingLiveDataViewModel
To introduce the terminology, here is a short introduction to the Architecture Components and how they work together. 
Note that this focuses on a subset of the components, namely LiveData, ViewModel and Room. 
Each component is explained more as you use it.

# To achieve this

 - Designed MainActivity: Display the data from database and take action from user.
 - Designed NewWordActivity: Add data in to the database
 - Designed Word: Model for the add record in database
 
 - Designed WordDao :Data access object. A mapping of SQL queries to functions. 
 When you use a DAO, you call the methods, and Room takes care of the rest.

 - Designed WordRepository:A class that you create that is primarily used to manage multiple data sources.
 
 - Designed WordRoomDatabase:Implifies database work and serves as an access point to the underlying SQLite database (hides SQLiteOpenHelper). 
 The Room database uses the DAO to issue queries to the SQLite database.
 
 - Designed WordViewModel: Acts as a communication center between the Repository (data) and the UI. 
 The UI no longer needs to worry about the origin of the data. 
 ViewModel instances survive Activity/Fragment recreation.
 
  - Designed WordListAdapter: Display the data in list format.

# Libraries & Dependency 


# Room components addedd dependencies
 
     implementation "androidx.room:room-runtime:$rootProject.roomVersion"
     kapt "androidx.room:room-compiler:$rootProject.roomVersion"
     implementation "androidx.room:room-ktx:$rootProject.roomVersion"
     androidTestImplementation "androidx.room:room-testing:$rootProject.roomVersion"

# Lifecycle components

    implementation "androidx.lifecycle:lifecycle-extensions:$rootProject.archLifecycleVersion"
    kapt "androidx.lifecycle:lifecycle-compiler:$rootProject.archLifecycleVersion"
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:$rootProject.archLifecycleVersion"

# Kotlin components

    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"
    api "org.jetbrains.kotlinx:kotlinx-coroutines-core:$rootProject.coroutines"
    api "org.jetbrains.kotlinx:kotlinx-coroutines-android:$rootProject.coroutines"

# Material design

    implementation "com.google.android.material:material:$rootProject.materialVersion"

# Testing

    testImplementation 'junit:junit:4.12'
    androidTestImplementation "androidx.arch.core:core-testing:$rootProject.coreTestingVersion"
    androidx.test.ext:junit:1.1.1
    androidx.test.espresso:espresso-core:3.2.0
   

# Setup the project in Android studio and run project.

1) Download the project code, preferably using git clone.

2) In Android Studio, select File | Open... and point to the ./build.gradle file.



