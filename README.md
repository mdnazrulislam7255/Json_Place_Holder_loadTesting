# JSON Place Holder Performance Testing
This project evaluates the performance of the JSON Place Holder fake API. Using Apache JMeter, this test plan is configured to simulate HTTP requests such as GET, POST, PUT, PATCH, and DELETE, targeting key API endpoints.

_**This test suite is designed to:**_
- Assess the system's responsiveness by measuring metrics like response time and throughput.
- Identify performance bottlenecks under increasing levels of concurrent user traffic.
- Ensure the API can handle typical operations like creating, updating, retrieving, and deleting bookings efficiently.

**Prerequisites**
1. _**System Requirements:**_
   - Operating System: Windows, Linux, or macOS
   - Java 8 or higher installed (required for JMeter)
2. _**Tools**_
   - Apache JMeter:  If you haven't already, [download and install Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi).
3. _**Setup and Execution**_
   - Step 1: Clone the Repository:
     ``` clone
       https://github.com/mdnazrulislam7255/Json_Place_Holder_loadTesting.git
     ```
   - Step 2: Configure JMeter
     Open the JsonPlaceholder.jmx file in Apache JMeter.
     Update the HTTP Request Defaults element to set the API base URL and authentication details (if applicable).
3. **_Import jmx file:_**
   - Open Jmeter.
   - Click on the Import button.
   - Select the file from the repository.

_**Usage**_ <br>

_**Select jmx file:**_ <br>
      In Apache JMeter, select the appropriate jmx file. <br>

_**Run project:**_ <br>                         																				
      Select the imported file. <br>
      Select any one of the listener . <br>
      Click Start Test to run the project.<br>
      
_**View Results:**_ <br>
       Once the tests are complete, view the results in the listener like View Results Tree or Aggregate Report. <br>
       Detailed test results can be viewed for each request.

## The script includes:
- Thread Groups: Configured with variable user loads and ramp-up times to simulate real-world usage patterns.
- HTTP Requests: Precisely configured for each API endpoint to validate CRUD operations.
- Assertions: Validates response status codes, response times, and data integrity.
- Listeners: Collect detailed test metrics and generate visual performance reports.

## Key API operations tested:
- GET /posts: Retrieve all posts.
- POST /posts: Create a new post with data.
- GET /posts/ID: Fetch details of a specific post.
- GET /posts/ID/ comments: Fetch details of a specific post and comments of the post.
- GET /comments?postId=1: Fetch a specific comment.
- PUT /posts: Update posts information.
- PATCH /posts/ID: Modify specific fields in a post.
- DELETE /posts/ID: Remove a post.

# Base URL
The base URL is: https://jsonplaceholder.typicode.com

# End points
## _Get Posts_
Protocol :_https_                                                                                                                                                                       
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                    
HTTP Request method: _GET_                                                                                                                                                                
Path: _/posts_                                                                                                                                                                            
Request body: ```none```                                                                                                                                                                  
Response body: ```Created```                                                                                                                                                             

## _Create Post_
Protocol : _https_                                                                                                                                                                        
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                         
HTTP Request method: _POST_                                                                                                                                                               
Path: _/posts_                                                                                                                                                                                                                                                                                                                                     
Request body:                                                                                                                                                                             
``` console
{
 
  "title": "New Post",
  "body": "This is the body of the new post."
}
```
Response body:
``` console
{
  "id": 101
}
```

## _Get Post by ID_
Protocol : _https_                                                                                                                                                                        
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                         
HTTP Request method: _GET_                                                                                                                                                               
Path: _/posts/1_                                                                                                                                                                         
Request body:                                                                                                                                                                             
``` console
None
```
Response body:
``` console
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```

## _Get Comments_
Protocol : _https_                                                                                                                                                                        
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                         
HTTP Request method: _GET_                                                                                                                                                               
Path: _posts/1/comments/_                                                                                                                                                                 
Request body:
``` none```                                                                                                                                                                               
Response body:
``` console
[
  {
    "postId": 1,
    "id": 1,
    "name": "id labore ex et quam laborum",
    "email": "Eliseo@gardner.biz",
    "body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
  },
  {
    "postId": 1,
    "id": 2,
    "name": "quo vero reiciendis velit similique earum",
    "email": "Jayne_Kuhic@sydney.com",
    "body": "est natus enim nihil est dolore omnis voluptatem numquam\net omnis occaecati quod ullam at\nvoluptatem error expedita pariatur\nnihil sint nostrum voluptatem reiciendis et"
  },
  {
    "postId": 1,
    "id": 3,
    "name": "odio adipisci rerum aut animi",
    "email": "Nikita@garfield.biz",
    "body": "quia molestiae reprehenderit quasi aspernatur\naut expedita occaecati aliquam eveniet laudantium\nomnis quibusdam delectus saepe quia accusamus maiores nam est\ncum et ducimus et vero voluptates excepturi deleniti ratione"
  },
  {
    "postId": 1,
    "id": 4,
    "name": "alias odio sit",
    "email": "Lew@alysha.tv",
    "body": "non et atque\noccaecati deserunt quas accusantium unde odit nobis qui voluptatem\nquia voluptas consequuntur itaque dolor\net qui rerum deleniti ut occaecati"
  },
  {
    "postId": 1,
    "id": 5,
    "name": "vero eaque aliquid doloribus et culpa",
    "email": "Hayden@althea.biz",
    "body": "harum non quasi et ratione\ntempore iure ex voluptates in ratione\nharum architecto fugit inventore cupiditate\nvoluptates magni quo et"
  }
]
```
## _Get Comments by ID_
Protocol : _https_                                                                                                                                                                        
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                         
HTTP Request method: _GET_                                                                                                                                                               
Path: _/comments?postId=1_                                                                                                                                                                
Request body:
``` none```                                                                                                                                                                               
Response body:
``` console
  [
  {
    "postId": 1,
    "id": 1,
    "name": "id labore ex et quam laborum",
    "email": "Eliseo@gardner.biz",
    "body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
  },
  {
    "postId": 1,
    "id": 2,
    "name": "quo vero reiciendis velit similique earum",
    "email": "Jayne_Kuhic@sydney.com",
    "body": "est natus enim nihil est dolore omnis voluptatem numquam\net omnis occaecati quod ullam at\nvoluptatem error expedita pariatur\nnihil sint nostrum voluptatem reiciendis et"
  },
  {
    "postId": 1,
    "id": 3,
    "name": "odio adipisci rerum aut animi",
    "email": "Nikita@garfield.biz",
    "body": "quia molestiae reprehenderit quasi aspernatur\naut expedita occaecati aliquam eveniet laudantium\nomnis quibusdam delectus saepe quia accusamus maiores nam est\ncum et ducimus et vero voluptates excepturi deleniti ratione"
  },
  {
    "postId": 1,
    "id": 4,
    "name": "alias odio sit",
    "email": "Lew@alysha.tv",
    "body": "non et atque\noccaecati deserunt quas accusantium unde odit nobis qui voluptatem\nquia voluptas consequuntur itaque dolor\net qui rerum deleniti ut occaecati"
  },
  {
    "postId": 1,
    "id": 5,
    "name": "vero eaque aliquid doloribus et culpa",
    "email": "Hayden@althea.biz",
    "body": "harum non quasi et ratione\ntempore iure ex voluptates in ratione\nharum architecto fugit inventore cupiditate\nvoluptates magni quo et"
  }
]
```

## _Update Post_
Protocol : _https_                                                                                                                                                                        
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                        
HTTP Request method: _PUT_                                                                                                                                                              
Path: _posts/1_                                                                                                                                                            
Request body:                                                         
                                                                                                                                                                             
``` console
 {
  
  "title": "Hello, Fooo",
  "body": "This is body part"
}
```
Response body:
``` console
{
  "id": 1
}
```
## _Update Post Partially_
Protocol : _https_
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                         
HTTP Request method: _PATCH_                                                                                                                                                              
Path: _posts/1_                                                                                                                                                               
Request body:                                                                                                                                                                             
``` console
{
	"title":"A Brieif History."
}

```
Response body:
``` console
{"id":1,"title":"A Brieif History."}
```

### _Delete post_                                                                                                                                                                 
Protocol : _https_                                                                                                                                                                        
Server Name or IP: _jsonplaceholder.typicode.com_                                                                                                                                         
HTTP Request method: _DELETE_                                                                                                                                                             
Path: _posts/1_                                                                                                                                                             
Request body: ``` none```                                                                                                                                                                 
Response body: ``` none```                                                                                                                                                             

### Run Command:
  Run Command for Report: Run from Jmeter bin folder where the project file is located
``` console
 jmeter -n -t JsonPlaceholder.jmx -l jsonplaceholder_api-3500\JsonPlaceholder.jtl

```
``` console
jmeter -g jsonplaceholder_api-3500\JsonPlaceholder.jtl -o jsonplaceholder_api-3500\JsonPlaceholder.html
```
### Reports
Test 1:
- Number of threads: _3500_; 
- Ramo-up period(seconds): _700_ ; 
- Loop count: _1_

  ![image](https://github.com/user-attachments/assets/54e82abd-c74f-443c-afb7-2a6577efa873)
  ![image](https://github.com/user-attachments/assets/7a46b68f-f89d-4ca9-87b9-351fb38ef6f3)
  ![image](https://github.com/user-attachments/assets/fea49576-50e7-4782-848a-f5c7c3e99e8a)


### Contact
For questions or support, contact the development team at: Email: _nazrul15-7255@diu.edu.bd_




