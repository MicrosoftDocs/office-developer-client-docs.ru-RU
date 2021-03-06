---
title: Функция CALLTHIS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Вызывает процедуру в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413817"
---
# <a name="callthis-function"></a>Функция CALLTHIS

Вызывает процедуру в проекте Microsoft Visual Basic для приложений (VBA).
  
## <a name="syntax"></a>Синтаксис

CALLTHIS(" ** *процедура* ** ",[" **** project ** "],[* *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _procedure_ <br/> |Обязательный  <br/> |**String** <br/> | Имя вызываемой процедуры.  <br/> |
| _проект_ <br/> |Необязательный  <br/> |**String** <br/> |Проект, содержащий процедуру.  <br/> |
| _arg_ <br/> |Необязательный  <br/> |**Число, строка, дата или валюта** <br/> |Передается в качестве параметров процедуры.  <br/> |
   
## <a name="remarks"></a>Примечания

В проекте VBA процедура  *определяется*  следующим образом: 
  
процедуры *(vsoShape* As Visio. Shape [arg1 As type, arg2 As type...]) 
  
где  *vsoShape*  является ссылкой на объект **Shape,** содержащий оцениваемую формулу CALLTHIS,  _и arg1_,  *arg2*  ... аргументы, указанные в этой формуле. 
  
Обратите  *внимание, что vsoShape*  очень похож на аргумент "этот", переданный процедуре участника C++; отсюда и имя "CALLTHIS". По сути, ячейку с формулой CALLTHIS можно прочитать так: "Вызывай эту процедуру и передай ссылку на мою фигуру". 
  
Если _задан_ проект, корпорация Майкрософт Visio все открытые документы  для одного из них, содержащего проект, и процедуру вызовов _в_ этом проекте. Если _проект_ опущен или null (""), Visio  предполагает, что процедура находится в проекте VBA документа, который содержит формулу CALLTHIS, которая оценивается. 
  
Номера  _в arg1,_  _arg2..._ передаются в внешних единицах. Например, если вы передаете значение ячейки Height из фигуры высотой 3 см, передается 3. Чтобы передать различные единицы с номером, используйте функцию FORMATEX или явно принудительные единицы, добавив null number-unit pair, например, 0 ft + Height. 
  
Вторая запятая в функции CALLTHIS необязательна. Это соответствует количеству дополнительных параметров, добавленных в процедуру. Если вы не используете какие-либо дополнительные параметры, за исключением, не добавляйте вторую запятую;  `(vsoShape as Visio.Shape)` используйте CALLTHIS ("",). Если вы добавляете два дополнительных параметра, например, используйте CALLTHIS (",,,). 
  
Функция CALLTHIS всегда оценивается до 0,  а вызов на процедуру возникает во время простоя после завершения процесса пересчета.  _Процедура_ может вернуть значение, но Visio игнорирует его.  _Процедура_ возвращает значение Visio которое можно распознать, установив формулу или результат другой ячейки в документе, но не ячейку, вызываемую процедурой, если вы не хотите перезаписать формулу CALLTHIS.
  
Функция CALLTHIS отличается от функции RUNADDON тем, что проекту документа не нужно ссылаться на другой проект для вызова в этот проект. 
  
> [!NOTE]
>  Код VBA, который вызывается, когда экземпляр Visio оценивает функцию CALLTHIS в формуле, не должен закрывать документ, содержащий ячейку с помощью функции, так как результаты ошибки приложения и Visio завершаются. 
  
Если необходимо закрыть документ, содержащий ячейку, использующую функцию CALLTHIS, используйте один из следующих методов: 
  
- Закрой документ из кода, который не является VBA.
    
- Закрой документ из проекта, кроме закрываемого.
    
- Вывешить сообщения о окне, чтобы закрыть окна в документе, а не закрыть документ.
    
Дополнительные сведения о запуске кода в Visio см. в Параметры и [running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой справке ShapeSheet. 
  
## <a name="example-1"></a>Пример 1

CALLTHIS ("p", FORMATEX(Height,#.00 u", "cm"))
  
Вызывает процедуру с именем p, расположенную в модуле, и передает значение Высоты в сантиметрах, например 7,62 см.
  
## <a name="example-2"></a>Пример 2

CALLTHIS ("q", 0 см+высота, ширина)
  
Вызывает процедуру q, расположенную в модуле, и передает высоту ячейки в сантиметры и ширину во внутренних единицах.
  
## <a name="example-3"></a>Пример 3

Используйте следующую процедуру в модуле *класса ThisDocument.* 
  
Используйте любой из следующих синтаксис в ячейке EventDblClick фигуры с предыдущими процедурами.
  
CALLTHIS ("ThisDocument.A",))
  
CALLTHIS ("ThisDocument.B", "Click")
  
CALLTHIS ("ThisDocument.C", "Click", "OK.")
  

