import requests
#setting more cookie
url ="https://httpbin.org/cookies/set?hi=hello&vysh=vyshu&data1=data2" #key-value pairs sent within the url
response = requests.get(url)
print(response) #printing response
print(response.text) #printing response text
print(response.status_code)   #printing status code
print(response.headers)    #printing headers
assert response.status_code == 200  #asserting whether status code is correct or not

#delete cookies
url="https://httpbin.org/cookies/delete?hi=hello"
hi = requests.get(url)
print(hi.text)
print(hi.status_code)
print(hi.headers)






