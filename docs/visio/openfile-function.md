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
description: Открывает документ Microsoft Visio, если он еще не открыт, и активирует окно документа.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419578"
---
# <a name="openfile-function"></a>Функция OPENFILE

Открывает документ Microsoft Visio, если он еще не открыт, и активирует окно документа.
  
## <a name="syntax"></a>Синтаксис

 **OPENFILE**( _"filename"_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Обязательно  <br/> |**Строка** <br/> |Имя файла, включая путь к файлу, который необходимо открыть.  <br/> |
   
## <a name="remarks"></a>Примечания

Несколько вызовов функций OPENFILE находятся в очереди и выполняются в порядке оценки. Если текущий документ Visio активирован для визуального редактирования (на месте), то будет запущен новый экземпляр Visio с именем запрашиваемого файла. 
  
Эта функция всегда возвращает false. 
  
В более ранних версиях приложения Visio эта функция отображается как _OPENFILE. Visio версий 4.0 и более поздних версий принимают любой стиль. 
  
## <a name="example"></a>Пример

 `OPENFILE("C:/MyFile.vsdx")`
  
Открывает указанный файл "MyFile.vsdx" в новом окне или активирует окно, если файл уже открыт. 
  

