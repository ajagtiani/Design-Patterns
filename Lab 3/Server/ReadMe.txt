Steps of Execution:

1. Run as administrator the Lab-3-Web-Service-1.0 application. The server should be running now.

2. When running your client program, add a service reference with the following link 

http://localhost:8731/Lab-3-Web-Service-1.0/Service1

3. The service contract has following two methods - 
	
    --	[OperationContract]
        void loadDictionary();
	
        Initializes a data structure with all the words from english-words.txt. This process happens only once when the server is running, no matter how many times you call this method from the client.This method has to be invoked first by the client in order to get a list of valid words or prefix after invoking the method getPredictiveText specified below.

	[OperationContract]
        List<String> getPredictiveText(String keyPresses);

	This method returns a list of valid words or valid prefix that can be formed from the Key Presses that is passed as a paramater to the method, otherwise, returns a string of hyphens whose length equals the length of keys pressed. The expected input parameter is a string of keypresses between the numbers 2-9.
	