---
title: Автоматизация InfoPath из внешнего приложения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath предоставляет автоматизации приложения из код, написанный с помощью COM и сценария с помощью методов объекта Application и коллекции XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807380"
---
# <a name="automating-infopath-from-an-external-application"></a>Автоматизация InfoPath из внешнего приложения

Microsoft InfoPath предоставляет автоматизации приложения из код, написанный с помощью COM и сценария с помощью методов объекта **Application** и коллекции **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Общие сведения о приложении и объектами XDocument

Объект **приложения** содержит следующие методы, используемые для автоматизации: 
  
|**Способ**|**Описание**|
|:-----|:-----|
|**CacheSolution** <br/> |Проверяет в кэше и, при необходимости обновляет его из места опубликования шаблона формы.  <br/> |
|**Завершите работу** <br/> |Завершает работу приложения Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Устанавливает указанный шаблон формы Microsoft Office InfoPath.  <br/> |
|**UnregisterSolution** <br/> |Удаляет указанный шаблон формы Microsoft Office InfoPath.  <br/> |
   
Коллекции **XDocuments** содержит следующие методы, которые могут быть использованы для внешней автоматизации. 
  
|**Способ**|**Описание**|
|:-----|:-----|
|Метод **Close**  <br/> |Закрывает указанную форму Microsoft Office InfoPath.  <br/> |
|Метод **New**  <br/> |Создает новую форму Microsoft Office InfoPath.  <br/> |
|Метод **NewFromSolution**  <br/> |Создает новую форму Microsoft Office InfoPath на основании указанного шаблона формы.  <br/> |
|Метод **NewFromSolutionWithData**  <br/> |Создает новую форму Microsoft Office InfoPath с помощью указанного шаблона формы и данные XML.  <br/> |
|Метод **Open**  <br/> |Открывает указанную форму Microsoft Office InfoPath.  <br/> |
   
Чтобы использовать объект **приложения** из внешнего приложения, используйте функции **CreateObject** с ProgID приложение InfoPath («InfoPath.Application») для создания переменной объекта, который представляет приложение InfoPath. Затем можно использовать свойство **XDocuments** для доступа к коллекции **XDocuments** и использовать его методы для откройте или создайте форму InfoPath. В следующем примере показано создание ссылки на объект **приложения** , с помощью Microsoft Visual Basic 6.0 или Visual Basic для приложений (VBA) языка программирования: 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Так как функции **CreateObject** создает объектную переменную с помощью позднего связывания, автоматическом завершении не будут доступны в редакторе Visual Basic. Обратитесь к ссылкам в таблицах выше сведения о правильный синтаксис вызова. 
  

