# B_tree_database_by_Cpp

## 목차
[1. Simple Class implementation](#simple-class-implementation)

[2. Class with File IO](#class-with-file-io)

[3. IOBuffer and BufferFile](#iobuffer-and-bufferfile)

[4. Recursive Compile Practice](#recursive-compile-practice)

[5. Indexed File](#indexed-file)

[6. Cosequential Processing](#cosequential-processing)

[7. B-Tree implementation Part1](#b-tree-implementation-part1)

[8. B-Tree implementation Part2](#b-tree-implementation-part2)

## Simple Class implementation

- Student클래스는 ID, 이름, 주 소, 첫 수강 날짜, 이수한 학점의 수를 멤버로 가지고 getter, setter, 
연산자 오버로딩함수를 추가한다. 

- CourseRegistration클래스는 강좌ID, 등록된 학생ID, 수업 시수, 성적을 멤버로 가지고 getter, setter
를 추가한다. 

- [source code](https://github.com/datalab-pnu/fs24hw1-sinsehwan)

## Class with File IO

- Student클래스에서 << 연산자와 >> 연산자를 오버로딩해서 객체 단위로 cout, cin이 가능하게 만들고 driver함수를 정의해서 점검한다. 

- CourceRegistration클래스에 <<연산자, >>연산자를 파일 스트림을 사용할 수 있도록 오버로딩하고 이를 통해 driver함수에서 파일 입출력이 가능한지 점검한다.

- [source code](https://github.com/datalab-pnu/fs24hw2-sinsehwan)

## IOBuffer and BufferFile

- Class with File IO에서 구현한 student 클래스와 CourseRegistration 클래스에 Pack과 UnPack 메소드를 추가하고 이를 IOBuffer 클래스에서 지원하는 버퍼 유형을 사용하여 테스트한다. 

- 추가적으로 데이터를 가독성 좋게 다루기 위해 char*형을 사용하지 않고 buffer를 string으로 선언해서 사용한다. 

- [source code](https://github.com/datalab-pnu/fs24hw4-sinsehwan)

## Recursive Compile Practice

- BufferFile 관련 내용, RecordFile 구현을 makefile이 하나인 하나의 폴더로 구현하지 말고 소스 코드를 폴더별로 분리하여 makefile을 Recursive하게 적용해보자. 

- [source code](https://github.com/datalab-pnu/fs24hw5-sinsehwan)

## Indexed File

- BufferFile, 재귀 컴파일을 사용하고 7장의 Indexing을 활용해서 Student클래스와 CourseRegistration 클래스를 인덱스로 접근가능하도록 설계한다.

- 이를 위해 IndexedFile 클래스를 정의해서 활용한다.

- [source code](https://github.com/datalab-pnu/fs24hw6-sinsehwan)

## Cosequential Processing

- 파일에 포함된 정보를 통해 학생 성적증명서와 학생 성적보고서를 생성해내는 프로그램을 설계한다.

- Ledge와 Journal처럼 학생 id 기준으로 매핑해서 보고서 형태로 출력가능하게 만들어보자. 

- [source code](https://github.com/datalab-pnu/fs24hw7-sinsehwan)

## B-Tree implementation Part1

- BTree 클래스와 BTreeNode클래스를 통해 B-Tree를 구현한다. BTreeNode의 경우 SimpleIndex를 상속받아서 구현한다. BTree 객체에서의 Insert와 Remove에서는 split, merge연산이 필요한지 점검하고 BTreeNode객체 리스트들을 통해 필요한 경우 BTreeNode의 split, merge, updateKey함수를 호출해서 BTree를 관리한다. 

-  BTree의 Remove함수와 BTree상태를 보기 위한 중위 순회 함수를 구현하고 Insert시에 BTree의 동작을 볼 수 있도록 만든다. 그리고 삽입과 삭제 모두 잘 동작하는지 테스트코드를 짜서 동작을 살펴본다. 
- Order는 5로 정한다.

- [source code](https://github.com/datalab-pnu/fs24hw8-sinsehwan)

## B-Tree implementation Part2

- BufferFile과 RecordFile에 B-Tree 인덱스를 추가한다. - 예제 파일 활용 오류로 인해 미완성

- [source code](https://github.com/datalab-pnu/fs24hw9-sinsehwan)

