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

RUNADDON(" *string*  ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Обязательно  <br/> |**Строка** <br/> | Имя надстройки в коллекции **Addons** или макроса в проекте VBA.  <br/> |
   
## <a name="remarks"></a>Примечания

Если проект документа, содержащий вызов функции RUNADDON (или другой проект, если на него есть ссылка), не содержит макрос (процедура без аргументов) с именем _строки,_ Microsoft Visio запускает именоваемую строку надстройки.  Если именоваемая строка надстройки не найдена, Visio ничего не делает и не сообщает об ошибке.  (С помощью свойства **TraceFlags** можно отслеживать процедуры и надстройки, которые пытается запустить Visio.) 
  
При вызове процедуры в стандартном модуле рекомендуется префиксировать строку с именем модуля, содержаменем модуля, содержаменем процедуры (например,  *moduleName.procName),* так как несколько модулей могут иметь процедуру с одинаковым именем. 
  
Чтобы вызвать процедуру в проекте, который не является проектом документа, который содержит вызов функции RUNADDON, используйте синтаксис  *projName.modName.procName*  (необходимо явно установить ссылку на  *projName в*  проекте VBA). 
  
> [!NOTE]
>  Начиная с Visio 2002 функция RUNADDON не может выполнять строку, содержащую произвольный код VBA. Код, который ранее был передан функции RUNADDON, может быть перемещен в процедуру в проекте VBA документа, который вызван из функции RUNADDON. 
  
Дополнительные сведения о запуске кода в Visio см. в справочнике по настройкам безопасности и запуску кода [в Visio.](about-security-settings-and-running-code-in-visio-shapesheet.md) 
  
В более ранних версиях Visio эта функция отображается как _RUNADDON. Visio версий 4.0 и более поздних версий принимают любой стиль. 
  
## <a name="example-1"></a>Пример 1

RUNADDON("Calendar.exe")
  
Запускает надстройки с названием Calendar.exe.
  
## <a name="example-2"></a>Пример 2

RUNADDON("Фигуры массива")
  
Запускает надстройки с именем Array Shapes (с реализацией VSL).
  
## <a name="example-3"></a>Пример 3

RUNADDON("ThisDocument.ReportStatistics")
  
Вызывает макрос ReportStatistics в модуле **ThisDocument** проекта документа, содержащего этот вызов функции. 
  
> [!NOTE]
>  Чтобы вызвать макрос в модуле **ThisDocument,** необходимо использовать перед строкой "ThisDocument", как показано ниже. 
  
## <a name="example-4"></a>Пример 4

RUNADDON(" *ModuleName*  . ReportStatistics") 
  
Вызывает макрос ReportStatistics в  *ModuleName*  в проекте документа, который содержит этот вызов функции. 
  

