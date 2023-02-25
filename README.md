# sahaj-airline# airline-ticket-discount

A major airline wants to send an email, offering a discount on upgrade to a higher class, to all the passengers who have booked tickets on its flights. For this, the data will be received in a file at a particular time. 

The program needs to read this data, perform some validations and then write it to a different file. The records that fail the validation, need to be put into a different file so that someone can look at them and fix the problem. Each failing record should have an additional field that will contain the reason(s) for the validation failure. 

Apart from the validation, we need to add a new column called discount code to the processed records file whose value will be calculated based on the fare class field in the input record. Fare class A - E will have discount code OFFER_20, F - K will have discount code OFFER_30, L - R will have OFFER_25; rest will have no offer code 


Input data will contain the following fields: 
● First name ● Last name ● PNR ● Fare class (Single character A - Z only) ● Travel date ● Pax (no of passengers) ● Ticketing date (the date of booking) ● Email ● Mobile phone ● Booked cabin (Economy, Premium Economy, Business, First) 

Validations: ● Email ID is valid ● The mobile phone is valid ● Ticketing date is before travel date ● PNR is 6 characters and Is alphanumeric ● The booked cabin is valid (one of Economy, Premium Economy, Business, First)

Sample data: 

For example, load data from a CSV file. 

Input data: First_name, Last_name, PNR, Fare_class, Travel_date, Pax, Ticketing_date, Email, Mobile_p hone, Booked_cabin A b h i s h e k , K u m a r , A B C 1 2 3 , F , 2 0 1 9 - 0 7 - 3 1 , 2 , 2 0 1 9 - 0 5 - 2 1 , abhishek@zzz.com, 9876543210, Economy Monin, Sankar, PQ234, C, 2019-08-30, 2, 2019-05-22, monin@zzz.com, 9876543211, Economy Radhika, Suresh, ZZZ345, T, 2019-05-31, 4, 2019-05-21, radhika@zzz, 9876543212, Business Kalyani, Ben, A1B2C3, M, 2019-04-30, 1, 2019-05-21, kben@zzz.com, 9876543213, Premium Economy Somnath, Batra, X1Y2Z4, Z, 2019-07-25, 3, 2019-05-23, sbatra@zzz.com, 9876543214, Economy 

Expected output: Successfully processed records: First_name, Last_name, PNR, Fare_class, Travel_date, Pax, Ticketing_date, Email, Mobile_p hone, Booked_cabin, Discount_code Abhishek, Kumar, ABC123, F, 2019-07-31, 2, 2019-05-21, abhishek@zzz.com, 9876543210, Economy, OFFER_30 Kalyani, Ben, A1B2C3, M, 2019-06-30, 1, 2019-05-21, kben@zzz.com, 9876543213, Premium Economy, OFFER_25 Somnath, Batra, X1Y2Z4, Z, 2019-07-25, 3, 2019-05-23, sbatra@zzz.com, 9876543214, Economy,

Failed records: First_name,Last_name,PNR,Fare_class,Travel_date,Pax,Ticketing_date,Email,Mobile_p hone,Booked_cabin,Error Monin, Sankar, PQ234, C, 2019-08-30, 2, 2019-05-22, monin@zzz.com, 9876543211, Economy, PNR invalid Radhika, Suresh, ZZZ345, T, 2019-05-31, 4, 2019-05-21, radhika@zzz, 9876543212, Business, Email invalid ![image](https://user-images.githubusercontent.com/95157524/218499981-34ff0753-6334-412c-bbbb-ba466ae49ac5.png)
[README.md](https://github.com/jagannath30691/sahaj-airline/files/10739730/README.md)

---------------------------------------------------------------------------------------------------------------------------------------------------------

Below are the step by step instructions to download the code , run the application 
and run the test cases.

Step-1:

To download the code in zip format go to Code->Download ZIP in the github repository

Step-2:

Extract the zip folder , after extraction the code will be present in
sahaj-airline-mvn folder.

Step-3:

To import the code in the local IDE go to File-Import-Existing Maven Project
give the root directory where the code is located in the local->select the pom file 
click on Next and Finish.

Step-4:

Once the project is imported in the IDE refresh the project and do the mvn 
clean install for the dependencies to get loaded.

Step-5:

To make the application up and running go to the SahajAirlineMvnApplication
right click -> run as Spring Boot App.

Step-6:

After this to see the files which were successful and failed go to sahaj-airline-mvn
src->main-> resources , there two files will be present airline-failed-out
and airline-success-out

Step-7:

In the above folder there are other two files airline-input file which
is provided by the airlines and airline-wrong-input file - this file is used for testing testing
purposes.

Step-8:

For running the test cases for the application got to SahajAirlineMvnApplicationtTests.java file in the com.sahaj.airline package
under src/test/java folder and right click on the file and Run As-Junit Test.

Step-9:

To run the test case for the genereated go to ReadCsvFileUtilTest.java file in com.sahaj.airline.util package.
under src/test/java folder and right click on the file and Run As-Junit Test.

Step-10:

To see the code coverage for the application go to ReadCsvFileUtilTest.java file in com.sahaj.airline.util package.
under src/test/java folder and right click on the file and Coverage As-Junit Test




