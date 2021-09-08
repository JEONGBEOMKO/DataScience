
### 1장 서울시 구별 CCTV 현황 분석

* 오타 수정
	* P34, In [26] 바로 위의 줄 df.loc[:, ['A', 'B']라고 --> **df.loc[:, ['A', 'B']]** 
	* P36, In [32] : df.iloc[[1,2,4],[0,2]] --> **In [32] : df.iloc[[1,2,4],[0:2]]** (
	* P38, In[40] df2['E'].isIn(['two','four']) --> **In[40] df2['E'].isin(['two','four'])** 
	* P40, In[44] x.mIn() --> **x.min()** (buillee님 감사합니다.)
	* P54, 밑에서 세 번째 줄, 0.7 이하면 뚜렷한 상관관계 --> **0.7 이상이면 뚜렸한 상관관계**
	* P57, In [95] np.arrange --> **np.arange** (김혁님 감사합니다.)

### 2장 서울시 범죄 현황 분석
* 구글 지도 API의 유료화 진행에 대해
	* **구글 지도 API가 최근 유료화 되었습니다. 그러나 학습용으로는 구글이 매월 200달러 규모의 크래딧을 지원하기 때문에 신용카드는 등록하더라도, 실제로 결재가 되지는 않을 것 같습니다.** 

* 코드가 변경된 사항
	* Matplotlib의 heatmap 등을 그릴때 cmap의 디폴트 설정이 변경되어 heatmap 등에서 cmap을 적용할 때 옵션을 잡아주어야 교재와 동일한 효과가 나타납니다. (소스코드에 모두 반영됨)
	* Folium이 0.4.0으로 판올림 되면서 choropleth 명령에서 geo_str 옵션명이 geo_data 옵션명으로 변경되었습니다. (소스코드에 모두 반영)
	* Folium이 0.4.0으로 판올림 되면서 circle marker 적용할때, fill=True 옵션을 반듯이 사용해야 합니다. (소스코드에 모두 반영)

### 3장 시카고 샌드위치 맛집 분석


*  코드가 변경된 사항
	* Folium이 0.4.0으로 판올림 되면서 choropleth 명령에서 geo_str 옵션명이 geo_data 옵션명으로 변경되었습니다.(소스코드에 모두 반영)
	* Folium이 0.4.0으로 판올림 되면서 circle marker 적용할때, fill=True 옵션을 반듯이 사용해야 합니다. (소스코드에 모두 반영)

### 4장 셀프 주유소는 정말 저렴할까


*  코드가 변경된 사항
	* Folium이 0.4.0으로 판올림 되면서 choropleth 명령에서 geo_str 옵션명이 geo_data 옵션명으로 변경되었습니다. (소스코드에 모두 반영)
	* Folium이 0.4.0으로 판올림 되면서 circle marker 적용할때, fill=True 옵션을 반듯이 사용해야 합니다. (소스코드에 모두 반영)

### 5장 우리나라 인구 소멸 위기 지역 분석

* 교재 대비 코드가 변경된 사항
	* Folium이 0.4.0으로 판올림 되면서 choropleth 명령에서 geo_str 옵션명이 geo_data 옵션명으로 변경되었습니다. (소스코드에 모두 반영)

### 6장 19대 대선 결과 분석

* 내용수정
	* 6장은 아주 큰 변화가 있습니다. 바로 분석 대상이 되는 선거관리위원회 홈페이지가 변경된 것입니다.
	* 그러나 6-3절 이후의 내용은 Github에서 배포하는 데이터를 이용해서 학습이 가능합니다.
	* 정상적으로 동작하는 코드는 다시 올려두었습니다. 세세한 내용은 해당 소스코드를 참조해 주세요.
		
* 교재 대비 코드가 변경된 사항
	* Folium이 0.4.0으로 판올림 되면서 choropleth 명령에서 geo_str 옵션명이 geo_data 옵션명으로 변경되었습니다. (소스코드에 모두 반영)

### 7장 시계열 데이터를 다뤄보자
* 교재 오류 수정
	
* 중요 변경 부분 : Pandas 주식 데이터 오류
	* 현재 구글이든 야후든 pandas의 주식 데이터를 읽어오는데 문제가 있습니다. 이미 github에서 꽤 issue가 되고 있는듯 하지만, 아직 해결방법이 있지는 않은듯 합니다.
	* 최근 이 문제를 해결하기 위한 방법을 고민해주는 고마운 분들이 만들어준 모듈이 있습니다.
	* 터미널에서 **pip install fix_yahoo_finance**로 fix_yahoo_finance를 설치하시고 아래와 같이 코드에서 사용하시면 됩니다.
	
	```python
	from pandas_datareader import data
	import fix_yahoo_finance as yf
	yf.pdr_override()

	start_date = '2010-03-01' 
	end_date = '2018-02-28' 
	KIA = data.get_data_yahoo('000270.KS', start_date, end_date)
	```

### 8장 자연어 처리 시작하기

* 모듈 설치
	* KoNLPy : **pip install konlpy**
	* JPype1 : **conda install -c conda-forge jpype1**
		* 이후 Jupyter Notebook 재실행 필요
	* JDK 설치 : Java JDK로 검색해서 OS에 맞춰 설치
   		* JAVA_HOME 설정 : 교재내용 참조 
   	* WordCloud 설치 : **pip install wordcloud**
	* gensim install : **pip install gensim**
	

