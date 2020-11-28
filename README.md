[![Build Status](https://travis-ci.com/UNIZAR-30246-WebEngineering/lab3-restful-ws.svg?branch=master)](https://travis-ci.com/UNIZAR-30246-WebEngineering/lab3-restful-ws)
# Web Engineering 2020-2021 / RESTful Web services
**In this assignment your PR must only modify the `README.md` file**.
Please, go to the [Wiki](https://github.com/UNIZAR-30246-WebEngineering/lab3-restful-ws/wiki) in order to get the instructions for this assignment.

## Primary goal

Complete the tests of `AddressBookServiceTest` to tests if the service meets the HTTP semantics.
Each test in `AddressBookServiceTest` is incomplete. 
For example, the method `serviceIsAlive` tests if: 

```http
GET /contacts
```

returns an empty list, but it must be extended in order to verify that `GET /contacts` meets the HTTP GET contract: 

- GET request is safe (it does not modify the contents of the address book)
- GET request is idempotent (two consecutive calls return the same).

> *Note: During the lab session was revealed that a subtle bug is hidden in the code that may cause you problems if the server has many concurrent requests. Finding this bug is not a requirement for this lab, but you must report me which flaw you suspect the code has (e.g. by adding a note in AddressBookServiceTest.java). I will accept your PR regardless your findings are correct or not, or even if you tell me you cannot find the bug. After accepting your PR, I will provide feedback by email on this bug if you cannot find it because I strongly believe that being aware of the problems that this bug causes and how to fix it will be helpful for your URL shortener project.*

## Secondary goals (:gift:)

Solutions must meet primary goals too. 

Done:

- [Replace the current implementation (Jakarta Jersey) by a Spring MVC (Servlet) implementation](https://github.com/rauljavierre/lab3-restful-ws/tree/test) was implemented by Raul Javierre. He has learned how to map concepts from JAX-RS to Spring MVC and how frameworks can help to obtain extra information from HTTP requests :gift:
- [CORS support](https://github.com/UNIZAR-30246-WebEngineering/lab3-restful-ws/pull/12) was implemented by Alvaro García on the original Jakarta Jersey implementation. His PR is explains how CORS works very clearly. Worth read :gift:
- [Use JWT credentials to grant access to requests](https://github.com/UNIZAR-30246-WebEngineering/lab3-restful-ws/pull/14) was implemented by Alberto Calvo on the original Jakarta Jersey implementation. How JWT support is implemented in frameworks may differ. For example, Spring Framework requires the use of a Filter in order to integrate JWT with Spring Security. However Jakarta Jersey is more clean and the implementation of Alberto makes easier to understand how JWT works on the server side :gift:
- [Support of OpenAPI 3.0](https://github.com/UNIZAR-30246-WebEngineering/lab3-restful-ws/pull/38) was implemented by Jorge García on the original Jakarta Jersy implementation. He has learned that documenting an API is an easy but tedious word. Also, it is an error prone task because the documentation may drift away from the implementation easily. 

Proposed:

- Replace the current implementation (Jakarta Jersey) by a [Spring WebFlux](https://docs.spring.io/spring-framework/docs/current/reference/html/web-reactive.html#spring-webflux) (Reactive) implementation
- Support asynchronous requests without using Spring WebFlux 
- Support of HTTP/2 requests 
- Support of HTTPS requests using self-signed certificate 

Note: unless the goal specifies o disallows a specific framework you are free to replace the framework used in the original implementation with a different framework.

Manifest your intention first by a PR updating this `README.md` with your goal.
If you desist of your goal, release it by a PR so other fellow can try it. 


| NIA    | User name | Repo | Build Status | Improvement | Score
|--------|-----------|------|--------------|-------------|--------
| 740491 |[José Ignacio Hernández](https://github.com/740491)|[740491/lab3-restful-ws](https://github.com/740491/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/740491/lab3-restful-ws.svg?branch=test)|  |
| 758803 |[Daniel González](https://github.com/Uncastellum/)|[Uncastellum/lab3-restful-ws](https://github.com/Uncastellum/lab3-restful-ws/tree/test)|![Build Status](https://travis-ci.com/Uncastellum/lab3-restful-ws.svg?branch=test)|                      |
| 758906 |[Raúl Javierre](https://github.com/rauljavierre/)|[rauljavierre/lab3-restful-ws](https://github.com/rauljavierre/lab3-restful-ws/tree/test)|![Build Status](https://travis-ci.com/rauljavierre/lab3-restful-ws.svg?branch=test)| Trying to reimplement with Spring MVC | :gift:                     |
| 757153 |[Fran-sw](https://github.com/Fran-sw) |[lab3-restful-ws](https://github.com/Fran-sw/lab3-restful-ws/tree/test)|[![Build Status](https://travis-ci.com/Fran-sw/lab3-restful-ws.svg)](https://travis-ci.com/Fran-sw/lab3-restful-ws)       | |                      |
| 758267 |[Pedro Allué](https://github.com/piter1902/) | [piter1902/lab3-restful-ws](https://github.com/piter1902/lab3-restful-ws/tree/test) | [![Build Status](https://travis-ci.com/piter1902/lab3-restful-ws.svg?branch=test)](https://travis-ci.com/piter1902/lab3-restful-ws) |             |
| 761319 |[Marcos Nuez](https://github.com/Markles02/)|[Markles01/lab3-restful-ws](https://github.com/Markles01/lab3-restful-ws/tree/test)|![Build Status](https://travis-ci.com/Markles01/lab3-restful-ws.svg?branch=test)|                      |
| 739202 |[Luis Garcia](https://github.com/luisgg98/)|[luisgg98/lab3-restful-ws](https://github.com/luisgg98/lab3-restful-ws/tree/tests)|[![Build Status](https://travis-ci.com/luisgg98/lab3-restful-ws.svg?branch=tests)](https://travis-ci.com/luisgg98/lab3-restful-ws)|                      |
| 760739 |[Alberto Calvo](https://github.com/AlbertoCalvoRubio) |[AlbertoCalvoRubio/lab3-restful-ws](https://github.com/AlbertoCalvoRubio/lab3-restful-ws/tree/test)|[![Build Status](https://travis-ci.com/AlbertoCalvoRubio/lab3-restful-ws.svg)](https://travis-ci.com/AlbertoCalvoRubio/lab3-restful-ws) | Trying to use JWT credentials to grant access to requests| :gift:|
| 760704 |[Álvaro García](https://github.com/Alvarogd6)|[Alvarogd6/lab3-restful-ws](https://github.com/Alvarogd6/lab3-restful-ws/tree/test)|![Build Status](https://travis-ci.com/Alvarogd6/lab3-restful-ws.svg?branch=test)| Support of [CORS](https://developer.mozilla.org/es/docs/Web/HTTP/Access_control_CORS) requests | :gift: |
| 756123 |[Rogelio Lacruz](https://github.com/RogorStuff)|[RogorStuff/lab3-restful-ws](https://github.com/RogorStuff/lab3-restful-ws/tree/test) |[![Build Status](https://travis-ci.org/RogorStuff/lab3-restful-ws.svg)](https://travis-ci.org/RogorStuff/lab3-restful-ws)| |                      |
| 766685 |[Enrique Ruiz Flores](https://github.com/TheRealFreeman)|[TheRealFreeman/lab3-restful-ws](https://github.com/TheRealFreeman/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/TheRealFreeman/lab3-restful-ws.svg?branch=test)|  |
| 755769 |[Saúl Flores Benavente](https://github.com/saul205)|[saul205/lab3-restful-ws](https://github.com/saul205/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/saul205/lab3-restful-ws.svg?branch=test)|  |
| 758325 |[Irene Fumanal](https://github.com/irefu/)|[irefu/lab3-restful-ws](https://github.com/irefu/lab3-restful-ws/tree/test)|![Build Status](https://travis-ci.com/irefu/lab3-restful-ws.svg?branch=test)|                      |
| 755742 |[Juan José Tambo Tambo](https://github.com/jtambo99)|[jtambo99/lab3-restful-ws](https://github.com/jtambo99/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/jtambo99/lab3-restful-ws.svg?branch=test)|  |
| 794429 |[Martín Gascón](https://github.com/764429)|[764429/lab3-restful-ws](https://github.com/764429/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/764429/lab3-restful-ws.svg?branch=test)|  |
| 761754 |[David Alloza](https://github.com/david-AT) | [david-AT/lab3-restful-ws](https://github.com/david-AT/lab3-restful-ws/tree/test) |![Build Status](https://travis-ci.com/david-AT/lab3-restful-ws.svg?branch=test)|             |
| 739324 |[Elena Morón Vidal](https://github.com/elenamv13) | [elenamv13/lab3-restful-wsl](https://github.com/elenamv13/lab3-restful-ws/tree/test)|![Build Status](https://travis-ci.com/elenamv13/lab3-restful-ws.svg?branch=test)| | |
| 756308 |[Álvaro Santamaría](https://github.com/SanTa45zgz)|[SanTa45zgz/lab3-restful-ws](https://github.com/SanTa45zgz/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/SanTa45zgz/lab3-restful-ws.svg?branch=test)|  |
| 719974 |[Sergio Martínez](https://github.com/Sergio-Martinez-97)|[Sergio-Martinez-97/lab3-restful-ws](https://github.com/Sergio-Martinez-97/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/Sergio-Martinez-97/lab3-restful-ws.svg?branch=test)|  |
| 738845 |[Víctor Martínez](https://github.com/viriannn)|[viriannn/lab3-restful-ws](https://github.com/viriannn/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/viriannn/lab3-restful-ws.svg?branch=test)|  |
| 758635 |[Daniel Huici Meseguer](https://github.com/Kifixo)|[Kifixo/lab3-restful-ws](https://github.com/Kifixo/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/Kifixo/lab3-restful-ws.svg?branch=test)|  |
| 738233 |[Sergio Torres](https://github.com/cul3bro)|[cul3bro/lab3-restful-ws](https://github.com/cul3bro/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/cul3bro/lab3-restful-ws.svg?branch=test)|  |
| 740241 |[Sergio Álvarez](https://github.com/sergio-alv)|[sergio-alv/lab3-restful-ws](https://github.com/sergio-alv/lab3-restful-ws/tree/test)| ![Build Status](https://api.travis-ci.org/sergio-alv/lab3-restful-ws.svg?branch=test) | |
| 737070 |[Daniel Barceló](https://github.com/DaniBarcelo) |[DaniBarcelo/lab3-restful-ws](https://github.com/DaniBarcelo/lab3-restful-ws/tree/test)|[![Build Status](https://travis-ci.com/DaniBarcelo/lab3-restful-ws.svg)](https://travis-ci.com/DaniBarcelo/lab3-restful-ws) | | |
| 757715 |[Hayk Kocharyan](https://github.com/hayk99)|[hayk99/lab3-restful-ws](https://github.com/hayk99/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/hayk99/lab3-restful-ws.svg?branch=test)|  |
| 757755 |[Andrés Otero García](https://github.com/andrewknoll) | [andrewknoll/lab3-restful-ws](https://github.com/andrewknoll/lab3-restful-ws/tree/test) |![Build Status](https://travis-ci.com/andrewknoll/lab3-restful-ws.svg?branch=test)|             |
| 758807 |[Jorge García](https://github.com/jgarciapueyo) | [jgarciapueyo/lab3-restful-ws](https://github.com/jgarciapueyo/lab3-restful-ws/tree/test) |![Build Status](https://travis-ci.com/jgarciapueyo/lab3-restful-ws.svg?branch=test) | Support of OpenAPI 3.0 | :gift: |
| 735041 |[Eduardo Díaz](https://github.com/ediazl)|[ediazl/lab3-restful-ws](https://github.com/ediazl/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/ediazl/lab3-restful-ws.svg?branch=test)|  |
| 737791 |[Alejandro Omist Casado](https://github.com/oumist)|[oumist/lab3-restful-ws](https://github.com/oumist/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/oumist/lab3-restful-ws.svg?branch=test)|  |
| 723883 |[Jorge Turbica](https://github.com/turbica)|[turbica/lab3-restful-ws](https://github.com/turbica/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/turbica/lab3-restful-ws.svg?branch=test)|  |
| 738737 |[Víctor Jarreta](https://github.com/VJarreta) | [VJarreta/lab3-restful-ws](https://github.com/VJarreta/lab3-restful-ws/tree/test) |[![Build Status](https://travis-ci.com/VJarreta/lab3-restful-ws.svg?branch=test)](https://travis-ci.com/github/VJarreta/lab3-restful-ws) | | |
| 764539 |[Eduardo Ruiz](https://github.com/eduardoRuizC)|[eduardoRuizC/lab3-restful-ws](https://github.com/eduardoRuizC/lab3-restful-ws/tree/test)| ![Build Status](https://travis-ci.com/eduardoRuizC/lab3-restful-ws.svg?branch=test)|  |
