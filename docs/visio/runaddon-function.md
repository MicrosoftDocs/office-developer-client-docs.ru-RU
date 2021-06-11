---
title: Функция RUNADDON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Выполняет надстройки или макрос в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432011"
---
# <a name="runaddon-function"></a>Функция RUNADDON

Выполняет надстройки или макрос в проекте Microsoft Visual Basic для приложений (VBA). 
  
## <a name="syntax"></a>Синтаксис

RUNADDON (" *строка*  ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Обязательный  <br/> |**String** <br/> | Имя надстройки в коллекции **Addons** или макроса в проекте VBA.  <br/> |
   
## <a name="remarks"></a>Примечания

Если проект документа, содержащий вызов функции RUNADDON (или другой проект, если он ссылается), не имеет макроса (процедура без аргументов) с именем строки, Microsoft Visio запускает строку с именем надстройки _._ Если строка с  именем надстройки не найдена, Visio ничего не делает и не сообщает об ошибке. (Свойство **TraceFlags** можно использовать для мониторинга процедур и надстройок, Visio попыток запуска.) 
  
При вызове процедуры в стандартном модуле рекомендуется префиксировать строку с именем модуля, содержатую процедуру (например,  *moduleName.procName),* так как несколько модулей могут иметь процедуру с тем же именем. 
  
Чтобы вызвать процедуру в проекте, не в проекте документа, который содержит вызов функции RUNADDON, используйте синтаксис  *projName.modName.procName*  (вы должны явно задать ссылку на  *projName*  в проекте VBA). 
  
> [!NOTE]
>  Начиная с Visio 2002 г. функция RUNADDON не может выполнять строку, содержащую произвольный код VBA. Код, который ранее был передан функции RUNADDON, может быть перемещен в процедуру в проекте VBA документа, который вызван из функции RUNADDON. 
  
Дополнительные сведения о запуске кода в Visio см. в Параметры и [running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой справке ShapeSheet. 
  
В более ранних версиях Visio эта функция отображается как _RUNADDON. Visio версии 4.0 и более поздние версии принимают любой стиль. 
  
## <a name="example-1"></a>Пример 1

RUNADDON ("Calendar.exe")
  
Запускает надстройка под названием Calendar.exe.
  
## <a name="example-2"></a>Пример 2

RUNADDON ("Формы массива")
  
Запускает надстройка (реализованная vsL) с именем Array Shapes.
  
## <a name="example-3"></a>Пример 3

RUNADDON ("ThisDocument.ReportStatistics")
  
Вызывает макрос ReportStatistics в модуле **ThisDocument** в проекте документа, содержащего этот вызов функции. 
  
> [!NOTE]
>  Чтобы вызвать макрос в модуле **ThisDocument,** необходимо предисловие строки с "ThisDocument", как показано. 
  
## <a name="example-4"></a>Пример 4

RUNADDON(" *ModuleName*  . ReportStatistics") 
  
Вызывает макрос ReportStatistics в  *ModuleName*  в проекте документа, который содержит этот вызов функции. 
  

