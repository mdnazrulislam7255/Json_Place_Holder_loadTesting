# JSON Place Holder Performance testing
This project evaluates the performance of the fake JSON Place Holder API. Using Apache JMeter, this test plan is configured to simulate HTTP requests such as GET, POST, PUT, PATCH, and DELETE, targeting key API endpoints.

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
       https://github.com/mdnazrulislam7255/Booking_API_Load_Testing.git
     ```
   - Step 2: Configure JMeter
     Open the JsonPlaceholder.jmx file in Apache JMeter.
     Update the HTTP Request Defaults element to set the API base URL and authentication details (if applicable).
3. **_Import collection:_**
   - Open Jmeter.
   - Click on the Import button.
   - Select the file from the repository.

**Usage**
_**Select Environment:**_
      In Apache JMeter, select the appropriate environment from the top-right dropdown.
_**Run Collection:**_
      Select the imported collection.
      Select any one of the listener .
      Select the desired environment.
      Click Start Test to run the project.
_**View Results:**_
     Once the tests are complete, view the results in the listener like View Results Tree or Aggregate Report.
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

## _Get post by ID_
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
## _Update posts Partially_
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
 jmeter -n -t Restful_Booker.jmx -l reports\Restful_Booker.jtl
```
``` console
 jmeter -g reports\Restful_Booker.jtl -o reports\Restful_Booker.html
```
### Reports
Test 1:
- Number of threads: _1400_; 
- Ramo-up period(seconds): _300_ ; 
- Loop count: _1_
                                                                                                                                                                      
![image](https://github.com/user-attachments/assets/c0eb883c-9d64-48b5-8f46-4e3f879c3ead)
![image](https://github.com/user-attachments/assets/2d3e7db6-d517-4ca9-b69b-54fddfcaac4a)
![image](https://github.com/user-attachments/assets/86ed5c8b-4fb2-46ac-ab39-be6314bc956b)

Test 2:
- Number of threads: _2500_; 
- Ramo-up period(seconds): _500_ ; 
- Loop count: _1_

![image](https://github.com/user-attachments/assets/bb5ea66d-12fa-4f75-aca2-7d937500c2c8)
![image](https://github.com/user-attachments/assets/ce58be70-068b-49f8-95eb-21fc2f05cdf7)
![image](https://github.com/user-attachments/assets/89637daf-b33a-4ddc-b050-a169aac052b5)

### Contact
For questions or support, contact the development team at: Email: _nazrul15-7255@diu.edu.bd_




