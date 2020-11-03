#  Crawling_Python
![zz](https://cdn.inflearn.com/wp-content/uploads/python_crawler.jpg) </br></br>
If you want to see metadata or get more detailed information on the data set, please refer to the link below.</br>
<https://www.dataquest.io/blog/web-scraping-tutorial-python/>
 
# 다양한 크롤링 라이브러리
파이썬으로 웹을 크롤링할수있는 라이브러리와 프레임워크는 매우 다양하다.</br>
그중 BeautifulSoap 와 Selenium 을 활용해보고자 한다.</br></br></br>

# 보면 좋을 순서 : Crawling(Beautifulsoap).ipynb --> Crawling(Selenium).ipynb --> mycrawling
위의 코드순서는 각각을 소개하고 mycrawling에서는 두개의 시간을 비교해보았다. </br>
더 빠른 속도를 낼수있는 코드는 언제든지 환영이다 ! Welcome to contribution
 ## Table of content
 
1. BeautifulSoup
2. Selenium
3. 차이
# 1. Requests or urlib(beautifulsoup)

beautifulsoap는 HTML, XML 파일의 정보를 추출해내는 python 라이브러리 이다.</br>

이 방식은 python 내장 모듈인 requests 혹은 urllib 을 이용해 HTML을 다운받고, beautifulsoup로 데이터를 추출하는 방식이다.</br>
해당 방식은 HTML을 다운 받기에 , 서버사이드렌더링을 사용하지않는 SPA 사이트나, javaScript 렌더링을 필요로하는 사이트들은 크롤링하기 어렵다고 한다.</br></br>


SPA 에 대한 설명 : https://m.blog.naver.com/PostView.nhn?blogId=azure0777&logNo=220812404024&proxyReferer=https:%2F%2Fwww.google.com%2F</br>
렌더링에 대한 설명 : https://tuhbm.github.io/2017/08/10/rendering1/</br></br>

장점 --> 쉽고 멀티프로세스 혹은 멀티 쓰레드 적용시엔 빠르다.</br>
단점 --> 렌더링이 필요한 사이트들을 크롤링하기 어려움. 병렬처리 로직을 별도로 작성하지 않으면 느린편</br>
</br></br>

# 2.Selenium
</br></br>
셀리니움은 웹 자동화 테스트(버튼클릭, 스크롤 조작)에 사용되는 프레임워크이다.</br>
셀리니움을 이용한 크롤러는 웹 페이지에서 javascript 렌더링을 통해 생성되는 데이터들을 손쉽게 가져올수있다.</br>
인터넷브라우저를 통해 크롤링을 하는 개념이라, 실제 보여지는 웹페이지의 전부를 가져올 수 있고 디버깅 방법 또한 직관적이다.</br>
하지만 실제 웹브라우저를 실행시키는 방법이기때문에 속도가 많이 느리고 메모리도 상대적으로 많이 차지한다.</br>
멀티프로세스를 사용해서 여러 브라우저를 크롤링하도록 하면 속도를 개선할수있다.</br>
셀리니움 사용시 도커를 사용하면 편리하다고한다. (아직 도커를 이용해서 크롤링을 해보진않았다 ㅠㅠ)</br>

</br></br>
장점 --> 사용바작 보는 웹 페이지의 모든 정보를 가져올 수 있다.</br>
단점 --> 느리고 메모리를 많이 차지한다.
