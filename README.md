# Flutter_Notes

### Flutter using clean Architecture

 --> Clean architecture helps you maintain your code and it's really suitable for large projects and best for scalability. Flutter beginners get difficult time to understand and implement it.

 --> Clean architecture itself follow something called SOLID.

![image](https://github.com/user-attachments/assets/0c9f7d96-6373-4ada-a000-15a52fd0976d)

**a) Domain layer**

   --> Domain layer contains the business logic of our application. But this is not BLoC business logic. Strongly suggest to write your code from domain layer.

  --> In general, domain layer works with presentation layer. Domain layer is triggered by an events from presentation layer. These events could be a button press or API calling.

  --> Domain does not depend on anyone. Presentation layer finds domain layer to work with.

   ![image](https://github.com/user-attachments/assets/5fdcee19-3deb-47af-aeec-8407d5558661)


**b) Data layer**

 --> Data layer is for fetching data from outside world or from local storage to app. Data layer depends on domain layer. If you delete domain layer, data layer will get error. But the opposite is not true. In general data layer contains three below folders.

  i) datasources
  ii) models
  iii) repos

  ![image](https://github.com/user-attachments/assets/38484f33-3e51-4b5a-a57c-f1e6891ee815)



 c) **Presentation layer** **

--> Presentation layer may include your bloc, views, utils, and widgets. This layer mostly depends on other layer.

  ![image](https://github.com/user-attachments/assets/f37d2e6f-a5eb-418b-86cb-c1779605d970)


   ![image](https://github.com/user-attachments/assets/e0910e76-f0e9-4344-99d0-35e78bd45330)


   **Question & Answers:**

  **i) Where does the domain layer sit?**

    It sits between data and presentation layer.

  **ii) How many sub direcotry does the domain layer have?**

    It will have three sub directories.

   **iii) What's the first thing in domain layer?**

     It's the entities folder. It would contain the blue print of the data coming from server. It's like our data structure.

   **iv) What does the domain layer's repository do?****

      Repositories contain contract between data layer and domain layer.

   ***v)How are the contracts defined?****

      They are defined using interfaces or abstract classes. 

  **vi) How are domain layers usecases and repository connected?**
  
      Usescases depend on the repositories.

   **vii) What principle does domain layer's usecases follow?**

        They follow SRP(Single Responsibility Principle) principle.
        
  **viii) In TDD, what do you test from the domain layer?**

      We test the usecases of domain layer.

  **ix) what else do usecases do?**

      They carry out the operations of repository.

   **x) What are models in data layer?**

      They are like entities with extra features.

   **xi) How does domain layer connects to data layer?**

       Domain layer's repos are implemented in data layer.

   **xii) What are the repos of data layer?**

        These repos are connected from the repos of the domain layer.

  **xiii) What is the datasources folder in data layer?**

      Datasources folder's dart files implement the repos of data layer.  This is the actual of implementation that's get triggerd from usecases of domain layer.

      They are the implementation of the domain layer's repo. Domain layer's repos are abstract classes

   **xiv) How does presentation layer reaches to domain layer?**

      Presentation layer does it through usecases. Usecases use something called callable() method in dart to reach to the repos of domain layer.

    







   
