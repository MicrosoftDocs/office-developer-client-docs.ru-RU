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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360958"
---
# <a name="openfile-function"></a>Функция OPENFILE

Открывает документ Microsoft Visio, если он еще не открыт, и активирует окно документа.
  
## <a name="syntax"></a>Синтаксис

 **OPENFILE** ( _"filename"_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _задан_ <br/> |Обязательный  <br/> |**String** <br/> |Имя файла, включая путь к файлу, который требуется открыть.  <br/> |
   
## <a name="remarks"></a>Примечания

Несколько вызовов функций OPENFILE ставятся в очередь и выполняются в порядке оценки. Если текущий документ Visio активирован для редактирования на визуальном (на месте), запускается новый экземпляр Visio с запрошенным именем файла. 
  
Эта функция всегда возвращает значение FALSE. 
  
В более ранних версиях приложения Visio Эта функция отображается как _ОПЕНФИЛЕ. Visio версии 4,0 и более поздних принимают любой из этих стилей. 
  
## <a name="example"></a>Пример

 `OPENFILE("C:/MyFile.vsdx")`
  
Открывает указанный файл "MyFile. vsdx" в новом окне или активирует окно, если файл уже открыт. 
  

