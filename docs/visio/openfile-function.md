---
title: Функция OPENFILE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Открывает документ microsoft Visio, если он еще не открыт, и активирует окно документа.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419578"
---
# <a name="openfile-function"></a>Функция OPENFILE

Открывает документ microsoft Visio, если он еще не открыт, и активирует окно документа.
  
## <a name="syntax"></a>Синтаксис

 **OPENFILE** _("filename"_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _имя файла_ <br/> |Обязательный  <br/> |**String** <br/> |Необходимо открыть имя файла, включая путь к файлу.  <br/> |
   
## <a name="remarks"></a>Примечания

Несколько вызовов функций OPENFILE в очереди и выполняются в порядке оценки. Если текущий Visio активирован для визуального (на месте) редактирования, Visio экземпляр с запрашиваемой именем файла. 
  
Эта функция всегда возвращает FALSE. 
  
В более ранних версиях приложения Visio эта функция отображается как _OPENFILE. Visio версии 4.0 и более поздние версии принимают любой стиль. 
  
## <a name="example"></a>Пример

 `OPENFILE("C:/MyFile.vsdx")`
  
Открывает указанный файл "MyFile.vsdx" в новом окне или активирует окно, если файл уже открыт. 
  

