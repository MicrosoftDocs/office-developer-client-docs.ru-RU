---
title: Автоматизация InfoPath из внешнего приложения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью COM и сценариев, с помощью методов объекта Application и коллекции XDocument.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412669"
---
# <a name="automating-infopath-from-an-external-application"></a>Автоматизация InfoPath из внешнего приложения

Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью COM и сценариев, с помощью методов объекта **Application** и коллекции **XDocument** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Общие сведения об объектах Application и XDocument

Объект **Application** содержит следующие методы, используемые для автоматизации: 
  
|**Метод**|**Описание**|
|:-----|:-----|
|**CacheSolution** <br/> |Проверяет в кэше и при необходимости обновляет его из расположения, в котором опубликован шаблон формы.  <br/> |
|**Quit** <br/> |Завершает работу приложения Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Устанавливает указанный шаблон формы Microsoft Office InfoPath.  <br/> |
|**UnregisterSolution** <br/> |Удаляет указанный шаблон формы Microsoft Office InfoPath.  <br/> |
   
Коллекция **XDocuments** содержит следующие методы, которые можно использовать для внешней автоматизации: 
  
|**Метод**|**Описание**|
|:-----|:-----|
|Метод **Close**  <br/> |ЗаКрывает указанную форму Microsoft Office InfoPath.  <br/> |
|Метод **New**  <br/> |Создает новую форму Microsoft Office InfoPath.  <br/> |
|Метод **NewFromSolution**  <br/> |Создает новую форму Microsoft Office InfoPath на основе указанного шаблона формы.  <br/> |
|Метод **невфромсолутионвисдата**  <br/> |Создает новую форму Microsoft Office InfoPath с помощью указанных XML-данных и шаблона формы.  <br/> |
|Метод **Open**  <br/> |Открывает указанную форму Microsoft Office InfoPath.  <br/> |
   
Чтобы использовать объект **Application** из внешнего приложения, используйте функцию **CreateObject** с ProgID приложения InfoPath ("InfoPath. Application"), чтобы создать объектную переменную, представляющую приложение InfoPath. Затем можно использовать свойство **XDocuments** для доступа к коллекции **XDocument** и использовать его методы для открытия или создания формы InfoPath. В приведенном ниже примере показано создание ссылки на объект **Application** с помощью языка программирования Microsoft Visual Basic 6,0 или Visual Basic для приложений (VBA). 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Так как функция **CreateObject** создает объектную переменную с помощью позднего связывания, автоматическое завершение операторов будет недоступно в редакторе Visual Basic. Чтобы получить сведения о правильном синтаксисе вызова, ознакомьтесь со ссылками, приведенными в предыдущих таблицах. 
  

