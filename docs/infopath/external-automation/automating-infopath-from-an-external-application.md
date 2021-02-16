---
title: Автоматизация InfoPath из внешнего приложения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью COM и скрипта, с помощью методов объекта Application и коллекции XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412669"
---
# <a name="automating-infopath-from-an-external-application"></a>Автоматизация InfoPath из внешнего приложения

Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью COM и скрипта, с помощью методов объекта **Application** и **коллекции XDocuments.** 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Обзор объектов Application и XDocument

Объект **Application** содержит следующие методы, используемые для автоматизации: 
  
|**Способ**|**Описание**|
|:-----|:-----|
|**CacheSolution** <br/> |Проверяет кэш и при необходимости обновляет его из опубликованного расположения шаблона формы.  <br/> |
|**Quit** <br/> |Выход из Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Устанавливает указанный Microsoft Office формы InfoPath.  <br/> |
|**UnregisterSolution** <br/> |При этом указанный шаблон Microsoft Office Формы InfoPath.  <br/> |
   
Коллекция **XDocuments** содержит следующие методы, которые можно использовать для внешней автоматизации: 
  
|**Способ**|**Описание**|
|:-----|:-----|
|Метод **Close**  <br/> |Закрывает указанную Microsoft Office InfoPath.  <br/> |
|**Новый** метод  <br/> |Создает новую Microsoft Office InfoPath.  <br/> |
|**Метод NewFromSolution**  <br/> |Создает новую Microsoft Office InfoPath на основе указанного шаблона формы.  <br/> |
|**Метод NewFromSolutionWithData**  <br/> |Создает новую Microsoft Office InfoPath с использованием указанных данных XML и шаблона формы.  <br/> |
|**Метод Open**  <br/> |Открывает указанную Microsoft Office InfoPath.  <br/> |
   
Чтобы использовать объект **Application** из внешнего приложения, используйте функцию **CreateObject** с progID приложения InfoPath ("InfoPath.Application"), чтобы создать объектную переменную, представляюную приложение InfoPath. Затем можно использовать свойство **XDocuments** для доступа к коллекции **XDocuments** и использовать его методы для открытия или создания формы InfoPath. В следующем примере показано создание ссылки на объект **Application** с помощью языка программирования Microsoft Visual Basic 6.0 или Visual Basic для приложений (VBA): 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Так как **функция CreateObject** создает объектную переменную с использованием поздней привязки, автоматическое завершение выполнения выписки не будет доступно в редакторе Visual Basic. Сведения о правильном синтаксише вызовов можно найти по ссылкам в предыдущих таблицах. 
  

