---
title: Автоматизация InfoPath из внешнего приложения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью com и скрипта с помощью методов объекта Приложения и коллекции XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412669"
---
# <a name="automating-infopath-from-an-external-application"></a>Автоматизация InfoPath из внешнего приложения

Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью com и скрипта с помощью методов объекта **Приложения** и **коллекции XDocuments.** 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Обзор объектов приложения и XDocument

Объект **Application** содержит следующие методы, используемые для автоматизации: 
  
|**Способ**|**Описание**|
|:-----|:-----|
|**CacheSolution** <br/> |Проверяет кэш и при необходимости обновляет его из опубликованного расположения шаблона формы.  <br/> |
|**Quit** <br/> |Бросает приложение Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Устанавливает указанный Microsoft Office шаблон формы InfoPath.  <br/> |
|**UnregisterSolution** <br/> |Uninstalls the specified Microsoft Office InfoPath form template.  <br/> |
   
Коллекция **XDocuments содержит** следующие методы, которые можно использовать для внешней автоматизации: 
  
|**Способ**|**Описание**|
|:-----|:-----|
|Метод **Close**  <br/> |Закрывает указанную форму Microsoft Office InfoPath.  <br/> |
|**Новый** метод  <br/> |Создает новую форму Microsoft Office InfoPath.  <br/> |
|**Метод NewFromSolution**  <br/> |Создает новую форму Microsoft Office InfoPath на основе указанного шаблона формы.  <br/> |
|**Метод NewFromSolutionWithData**  <br/> |Создает новую форму Microsoft Office InfoPath с помощью указанных XML-данных и шаблона форм.  <br/> |
|**Метод Open**  <br/> |Открывает указанную форму Microsoft Office InfoPath.  <br/> |
   
Чтобы использовать объект **Application** из внешнего приложения, вы используете функцию **CreateObject** с помощью ProgID приложения InfoPath ("InfoPath.Application"), чтобы создать переменную объекта, которая представляет приложение InfoPath. Затем вы можете использовать **свойство XDocuments** для доступа к **коллекции XDocuments** и использовать его методы для открытия или создания формы InfoPath. В следующем примере показано создание ссылки на объект **Application** с помощью языка программирования Microsoft Visual Basic 6.0 или Visual Basic для приложений (VBA): 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Так как **функция CreateObject** создает переменную объекта с использованием поздней привязки, автоматическое завершение заявления не будет доступно в редакторе Visual Basic. Обратитесь к ссылкам в предыдущих таблицах, чтобы получить сведения о правильном синтаксис вызова. 
  

