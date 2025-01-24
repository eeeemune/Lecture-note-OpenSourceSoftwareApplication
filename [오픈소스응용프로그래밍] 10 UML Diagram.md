# [오픈소스응용프로그래밍] 10. UML Diagram

<aside>

# 💖 UML

</aside>

## UML이란?

<aside>

**UML(Unified Modeling Languate)**

**시스템을 시각적으로 설계하고 문서화**하는 데에 사용되는 표준화된 모델링 언어

</aside>

- 마치 DB의 E-R모델같은 개념이라고 생각하면 이해가 쉽습니다.
- 아래와 같은 12개의 diagram을 사용합니다.
    
    ![image.png](image%2010.png)
    

## UML Diagram

### ⚡ class

세 칸의 직사각형으로 클래스를 표현합니다.

| 클래스 이름 |
| --- |
| attributes |
| methods |

![image.png](image%2011.png)

### ⚡ visibility

UML Diagram에서 visiblity를 표시하는 방식입니다. visibility는 class의 구성 요소가 public인지, protoected인지, private인지에 따라 나뉩니다.

- `+` public
- `#`: protected
- `-`: private