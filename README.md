# demo-springdoc-openapi
Code for demo of springdoc openapi library to generate the open api spec automatically

Run the application, api spec is available at [/custom](http://localhost:8080/custom)

springdoc-openapi-ui module is used to serve the api spec as swagger ui for clear documentation. Add the below dependency in pom for swagger ui
		<dependency>
			<groupId>org.springdoc</groupId>
			<artifactId>springdoc-openapi-ui</artifactId>
			<version>${springdoc.version}</version>
		</dependency>
    
Api swagger documentation is available at 
http://localhost:8080/custom-ui.html

These paths can be modified in application.yml file of the application

## Guidelines
1. Open api bean needs to be there which will be initialised at startup.
2. Metadata for the project and apis like title, description, etc can be added in OpenApi class.
3. Springdoc scan the apis for spring annotations, like @ResponseStatus, @GetMapping, etc to get information about the api
4. Models are automatically recognised as schema in open api spec by spring doc.
5. Known issue: When you change the hosted path where api documentation are available, then refresh cookies and cache of browser to get documentation at new link or use incognito window.


## Screenshots

<img width="1689" alt="Screenshot 2022-05-26 at 10 52 16 AM" src="https://user-images.githubusercontent.com/95530856/170421695-767be2b7-839a-45a0-8284-13bd42d4c4d9.png">

<img width="1618" alt="Screenshot 2022-05-26 at 10 52 44 AM" src="https://user-images.githubusercontent.com/95530856/170421741-c59d4c11-a219-4701-a14f-5cceb98db21d.png">

<img width="1623" alt="Screenshot 2022-05-26 at 10 53 41 AM" src="https://user-images.githubusercontent.com/95530856/170421887-cdd4dd80-11ae-42c7-9bd7-9676fc7817b8.png">

<img width="1624" alt="Screenshot 2022-05-26 at 10 54 15 AM" src="https://user-images.githubusercontent.com/95530856/170421963-83b554eb-0fcc-408c-9630-a24765c01dec.png">

