---
title: Функция RUNADDONWARGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Выполняет строку и передает аргументы командной строки в программу в качестве строки.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408707"
---
# <a name="runaddonwargs-function"></a>Функция RUNADDONWARGS

Выполняет  _строку_ и передает аргументы  _командной_ строки в программу в качестве строки. 
  
## <a name="syntax"></a>Синтаксис

RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Обязательно  <br/> |**Строка** <br/> | Имя надстройки.  <br/> |
| _arguments_ <br/> |Обязательно  <br/> |**Строка** <br/> |Аргументы для передачи в программу.  <br/> |
   
## <a name="remarks"></a>Примечания

На практике  _аргументы должны_ иметь не более 50 символов. Используйте функцию RUNADDONWARGS для привязки программы, например надстройки, к ячейке, например к ячейке Action или Events. 
  
Функция RUNADDONWARGS может запускать только надстройки, которые являются членами коллекции **Addons приложения.** Чтобы она присутствовала в этой коллекции, надстройка должна быть EXE-файлом или VSL-файлом, который: 
  
- Устанавливается в пути  запуска или **надстройки** приложения. 
    
- Добавлено программным способом с помощью метода **Add** коллекции **Addons.** 
    
Дополнительные сведения о запуске кода в Visio см. в справочнике по настройкам безопасности и запуску кода [в Visio.](about-security-settings-and-running-code-in-visio-shapesheet.md) 
  
В более ранних версиях Visio эта функция отображается как _RUNADDONWARGS. Приложения Visio версий 4.0 и более поздних версий принимают любой стиль.
  
## <a name="example"></a>Пример

RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack") 
  
Запускает надстройку Graphmkr.exe и передает ему аргумент /GraphMaker=Stack. 
  

