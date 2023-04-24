## Spring Annotation - 지속적 update 
- @Controller - Controller의 역할(Model 객체를 사용하여 View 반환)을 수행하는 Class인것을 알려줌
- @ResponseBody - 자바 객체를 HttpResponse의 responseBody의 내용으로 매핑하는 역할을 수행한다.
- @RestController - @Controller에 @ResponseBody가 추가 된것으로 Json/XML 형태로 객체 데이터를 반환.
- @RequestMapping - 요청받을 URL과 value에 설정, method를 설정하면 같은 요청이 왔을 시에 RequestMapping으로 연결 시켜준다. 
- @{Method}Mapping - @RequestMapping을 이용해서 모두 설정해주면 길어지고 불편해지게 된다. 해서 Get,Post,Patch 등으로 명시할 수도 있다.\
- @RequestBody - HttpRequest에 담겨오는 body를 자바객체로 변환해준다. XML/JSON 기반의 메시지를 사용한다면 body의 데이터 통째로 VO로 매핑해준다.
- @ExceptionHandler - Controller에서 발생하는 에러를 가져와 메소드로 처리해준다. 구체적인 Exception을 적어주는 것이 좋다.
- @ResponseStatus - HttpResponse의 응답 상태를 설정해주는 어노테이션, HttpStatus Enum 클래스를 사용해 값을 넣어준다.