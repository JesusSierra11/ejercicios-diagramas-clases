# Ejercicios diagramas de clases
**Imagén original**:

![](/imagenes/pet.jpg)

**Diagrama creado con la herramienta Mermaid**:
[![](https://mermaid.ink/img/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG5BbmltYWwgPHwtLSBDYXQgOiBleHRlbmRzXG5BbmltYWwgPHwtLSBTcGlkZXIgOiBleHRlbmRzXG5BbmltYWwgPHwtLSBGaXNoIDogZXh0ZW5kc1xuUGV0IDx8Li4gRmlzaCA6IGltcGxlbWVudHNcblBldCA8fC4uIENhdCA6aW1wbGVtZW50c1xuICAgY2xhc3MgQW5pbWFse1xuICAgPDxhYnN0cmFjdD4-XG4gICAjbGVncyA6IGludFxuICAgI0FuaW1hbCAobGVncyA6IGludClcbiAgICt3YWxrKCkgdm9pZFxuICAgK2VhdCgpIHZvaWRcbiAgIH1cbiAgIGNsYXNzIFBldHtcbiAgIDw8aW50ZXJmYWNlPj5cbiAgICtnZXROYW1lKCkgU3RyaW5nXG4gICArc2V0TmFtZSAobiA6IFN0cmluZykgdm9pZFxuICAgK3BsYXkoKSB2b2lkXG4gICB9XG4gICBjbGFzcyBTcGlkZXJ7XG4gICArU3BpZGVyKClcbiAgICtlYXQoKSB2b2lkXG4gICB9XG4gICBjbGFzcyBDYXR7XG4gICAtbmFtZSA6IFN0cmluZ1xuICAgK0NhdCgpXG4gICArQ2F0IChuIDogU3RyaW5nKVxuICAgK2dldE5hbWUoKSBTdHJpbmdcbiAgICtzZXROYW1lKG4gOiBTdHJpbmcpIHZvaWRcbiAgICtwbGF5KCkgdm9pZFxuICAgK2VhdCgpIHZvaWRcbiAgIH1cbiAgIGNsYXNzIEZpc2h7XG4gICAtbmFtZSA6IFN0cmluZ1xuICAgK0Zpc2goKVxuICAgK2dldE5hbWUoKSBTdHJpbmdcbiAgICtzZXROYW1lKG4gOiBTdHJpbmcpIHZvaWRcbiAgICtwbGF5KCkgdm9pZFxuICAgK3dhbGsoKSB2b2lkXG4gICArZWF0KCkgdm9pZFxuICAgfVxuICAgICAgICAgICAgIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQifSwidXBkYXRlRWRpdG9yIjpmYWxzZX0)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG5BbmltYWwgPHwtLSBDYXQgOiBleHRlbmRzXG5BbmltYWwgPHwtLSBTcGlkZXIgOiBleHRlbmRzXG5BbmltYWwgPHwtLSBGaXNoIDogZXh0ZW5kc1xuUGV0IDx8Li4gRmlzaCA6IGltcGxlbWVudHNcblBldCA8fC4uIENhdCA6aW1wbGVtZW50c1xuICAgY2xhc3MgQW5pbWFse1xuICAgPDxhYnN0cmFjdD4-XG4gICAjbGVncyA6IGludFxuICAgI0FuaW1hbCAobGVncyA6IGludClcbiAgICt3YWxrKCkgdm9pZFxuICAgK2VhdCgpIHZvaWRcbiAgIH1cbiAgIGNsYXNzIFBldHtcbiAgIDw8aW50ZXJmYWNlPj5cbiAgICtnZXROYW1lKCkgU3RyaW5nXG4gICArc2V0TmFtZSAobiA6IFN0cmluZykgdm9pZFxuICAgK3BsYXkoKSB2b2lkXG4gICB9XG4gICBjbGFzcyBTcGlkZXJ7XG4gICArU3BpZGVyKClcbiAgICtlYXQoKSB2b2lkXG4gICB9XG4gICBjbGFzcyBDYXR7XG4gICAtbmFtZSA6IFN0cmluZ1xuICAgK0NhdCgpXG4gICArQ2F0IChuIDogU3RyaW5nKVxuICAgK2dldE5hbWUoKSBTdHJpbmdcbiAgICtzZXROYW1lKG4gOiBTdHJpbmcpIHZvaWRcbiAgICtwbGF5KCkgdm9pZFxuICAgK2VhdCgpIHZvaWRcbiAgIH1cbiAgIGNsYXNzIEZpc2h7XG4gICAtbmFtZSA6IFN0cmluZ1xuICAgK0Zpc2goKVxuICAgK2dldE5hbWUoKSBTdHJpbmdcbiAgICtzZXROYW1lKG4gOiBTdHJpbmcpIHZvaWRcbiAgICtwbGF5KCkgdm9pZFxuICAgK3dhbGsoKSB2b2lkXG4gICArZWF0KCkgdm9pZFxuICAgfVxuICAgICAgICAgICAgIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQifSwidXBkYXRlRWRpdG9yIjpmYWxzZX0)

En el original en la interfaz Pet, el metodo play() no tenía retorno, le he añadido el void.

## Código: 
   classDiagram
   Animal <|-- Cat : extends
   Animal <|-- Spider : extends
   Animal <|-- Fish : extends
   Pet <|.. Fish : implements
   Pet <|.. Cat :implements
   class Animal{
   <<abstract>>
   #legs : int
   #Animal (legs : int)
   +walk() void
   +eat() void
   }
   class Pet{
   <<interface>>
   +getName() String
   +setName (n : String) void
   +play() void
   }
   class Spider{
   +Spider()
   +eat() void
   }
   class Cat{
   -name : String
   +Cat()
   +Cat (n : String)
   +getName() String
   +setName(n : String) void
   +play() void
   +eat() void
   }
   class Fish{
   -name : String
   +Fish()
   +getName() String
   +setName(n : String) void
   +play() void
   +walk() void
   +eat() void
   }
         
**Imagén original**:

![](/imagenes/lectura.png)

**Diagrama creado con la herramienta Mermaid**:
[![](https://mermaid.ink/img/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG5DdXN0b21lclwiblwiLS08XCIxXCJSZWFkaW5nSXRlbTpidXlcbkdzdENoYXJnZWFibGUgPHwuLiBFbmN5Y2xvcGVkaWFcbkdzdENoYXJnZWFibGUgPHwuLiBNYWdhemluZVxuUmVhZGluZ0l0ZW0gPHwtLSBFbmN5Y2xvcGVkaWFcblJlYWRpbmdJdGVtIDx8LS0gTWFnYXppbmVcblJlYWRpbmdJdGVtIDx8LS0gQm9va1xuIGNsYXNzIEN1c3RvbWVye1xuIC1jdXN0b21lck5hbWUgOiBTdHJpbmdcbiAtdG90YWxQYXkgOiBkb3VibGVcbiBcbiArQ3VzdG9tZXIoU3RyaW5nKSB2b2lkXG4gK2J1eShSZWFkaW5nSXRlbSkgdm9pZFxuICtnZXRUb3RhbFBheSgpIGRvdWJsZVxuICt0b1N0cmluZygpIFN0cmluZ1xuIH1cbiBjbGFzcyBSZWFkaW5nSXRlbXtcbiA8PGFic3RyYWN0Pj5cbiAtdGl0bGUgOiBTdHJpbmdcbiAtcHJpY2UgOiBkb3VibGVcbiArUmVhZGluZ0l0ZW0oKSB2b2lkXG4gK1JlYWRpbmdJdGVtKGRvdWJsZSwgU3RyaW5nKSB2b2lkXG4gK2dldE5hbWUoKSBTdHJpbmdcbiArZ2V0UHJpY2UoKSBkb3VibGVcbiArY2FsY3VsYXRlUHJpY2UoKSpkb3VibGVcbiArZGlzcGxheUluZm8oKSogdm9pZFxuIH1cbiBjbGFzcyBHc3RDaGFyZ2VhYmxle1xuIDw8aW50ZXJmYWNlPj5cbiAtUkFURT0wLjA2IDogZG91YmxlIH5yZWFkT25seX5cbiArZ2V0R3N0Q2hhcmdlcygpIGRvdWJsZVxuIH1cbiBjbGFzcyBFbmN5Y2xvcGVkaWF7XG4gLXllYXIgOiBpbnRcbiArRW5jeWNsb3BlZGlhKCkgdm9pZFxuICtFbmN5Y2xvcGVkaWEoU3RyaW5nLCBkb3VibGUsIGludCkgdm9pZFxuIH1cbiBjbGFzcyBNYWdhemluZXtcbiAtbW9udGhJc3N1ZSA6IGludFxuIC15ZWFyIDogaW50XG4gK01hZ2F6aW5lKCkgdm9pZFxuICtNYWdhemluZShpbnQsIGludCwgZG91YmxlLCBTdHJpbmcpIHZvaWQgXG4gfVxuIGNsYXNzIEJvb2t7XG4gLWF1dGhvciA6IFN0cmluZ1xuIC15ZWFyIDogaW50XG4gK0Jvb2soKSB2b2lkXG4gK0Jvb2soU3RyaW5nLCBkb3VibGUsIFN0cmluZywgaW50KSB2b2lkXG4gfSIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0In0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG5DdXN0b21lclwiblwiLS08XCIxXCJSZWFkaW5nSXRlbTpidXlcbkdzdENoYXJnZWFibGUgPHwuLiBFbmN5Y2xvcGVkaWFcbkdzdENoYXJnZWFibGUgPHwuLiBNYWdhemluZVxuUmVhZGluZ0l0ZW0gPHwtLSBFbmN5Y2xvcGVkaWFcblJlYWRpbmdJdGVtIDx8LS0gTWFnYXppbmVcblJlYWRpbmdJdGVtIDx8LS0gQm9va1xuIGNsYXNzIEN1c3RvbWVye1xuIC1jdXN0b21lck5hbWUgOiBTdHJpbmdcbiAtdG90YWxQYXkgOiBkb3VibGVcbiBcbiArQ3VzdG9tZXIoU3RyaW5nKSB2b2lkXG4gK2J1eShSZWFkaW5nSXRlbSkgdm9pZFxuICtnZXRUb3RhbFBheSgpIGRvdWJsZVxuICt0b1N0cmluZygpIFN0cmluZ1xuIH1cbiBjbGFzcyBSZWFkaW5nSXRlbXtcbiA8PGFic3RyYWN0Pj5cbiAtdGl0bGUgOiBTdHJpbmdcbiAtcHJpY2UgOiBkb3VibGVcbiArUmVhZGluZ0l0ZW0oKSB2b2lkXG4gK1JlYWRpbmdJdGVtKGRvdWJsZSwgU3RyaW5nKSB2b2lkXG4gK2dldE5hbWUoKSBTdHJpbmdcbiArZ2V0UHJpY2UoKSBkb3VibGVcbiArY2FsY3VsYXRlUHJpY2UoKSpkb3VibGVcbiArZGlzcGxheUluZm8oKSogdm9pZFxuIH1cbiBjbGFzcyBHc3RDaGFyZ2VhYmxle1xuIDw8aW50ZXJmYWNlPj5cbiAtUkFURT0wLjA2IDogZG91YmxlIH5yZWFkT25seX5cbiArZ2V0R3N0Q2hhcmdlcygpIGRvdWJsZVxuIH1cbiBjbGFzcyBFbmN5Y2xvcGVkaWF7XG4gLXllYXIgOiBpbnRcbiArRW5jeWNsb3BlZGlhKCkgdm9pZFxuICtFbmN5Y2xvcGVkaWEoU3RyaW5nLCBkb3VibGUsIGludCkgdm9pZFxuIH1cbiBjbGFzcyBNYWdhemluZXtcbiAtbW9udGhJc3N1ZSA6IGludFxuIC15ZWFyIDogaW50XG4gK01hZ2F6aW5lKCkgdm9pZFxuICtNYWdhemluZShpbnQsIGludCwgZG91YmxlLCBTdHJpbmcpIHZvaWQgXG4gfVxuIGNsYXNzIEJvb2t7XG4gLWF1dGhvciA6IFN0cmluZ1xuIC15ZWFyIDogaW50XG4gK0Jvb2soKSB2b2lkXG4gK0Jvb2soU3RyaW5nLCBkb3VibGUsIFN0cmluZywgaW50KSB2b2lkXG4gfSIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0In0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)
  
En este diagrama he quitado el atributo item de tipo ReadingItem de la clase Customer porque al tener relación con ReadingItem, ya no le hace falta tenerlo a la clase Customer.
En el método getName() de la clase ReadingItem, en la imagen original viene con el valor de retorno void y yo lo he cambiado y le he puesto que el valor de retorno es un String.
Yo en la relación, he interpretado que el cliente compra 1 libro y los libros pueden ser comprados por muchos clientes.
## Código:

classDiagram
Customer"n"--<"1"ReadingItem:buy
GstChargeable <|.. Encyclopedia
GstChargeable <|.. Magazine
ReadingItem <|-- Encyclopedia
ReadingItem <|-- Magazine
ReadingItem <|-- Book
 class Customer{
 -customerName : String
 -totalPay : double
 
 +Customer(String) void
 +buy(ReadingItem) void
 +getTotalPay() double
 +toString() String
 }
 class ReadingItem{
 <<abstract>>
 -title : String
 -price : double
 +ReadingItem() void
 +ReadingItem(double, String) void
 +getName() String
 +getPrice() double
 +calculatePrice()*double
 +displayInfo()* void
 }
 class GstChargeable{
 <<interface>>
 -RATE=0.06 : double ~readOnly~
 +getGstCharges() double
 }
 class Encyclopedia{
 -year : int
 +Encyclopedia() void
 +Encyclopedia(String, double, int) void
 }
 class Magazine{
 -monthIssue : int
 -year : int
 +Magazine() void
 +Magazine(int, int, double, String) void 
 }
 class Book{
 -author : String
 -year : int
 +Book() void
 +Book(String, double, String, int) void
 }
