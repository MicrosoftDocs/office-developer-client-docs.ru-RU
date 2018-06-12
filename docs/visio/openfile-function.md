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
description: Открывает документ Microsoft Visio, если он еще не открыт и активирует окно документа.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814319"
---
# <a name="openfile-function"></a>Функция OPENFILE

Открывает документ Microsoft Visio, если он еще не открыт и активирует окно документа.
  
## <a name="syntax"></a>Синтаксис

 **OPENFILE** ( _«имя файла»_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Имя файла_ <br/> |Обязательный  <br/> |**Строка** <br/> |Имя файла, включая путь к файлу, который необходимо открыть.  <br/> |
   
## <a name="remarks"></a>Замечания

Несколько вызовов функций OPENFILE в очередь и выполняются в порядок вычисления. Если текущий документ Visio активирован для визуального редактирования (на месте), новый экземпляр Visio запускается с именем запрошенный файл. 
  
Эта функция всегда возвращает значение FALSE. 
  
В более ранних версиях приложения Visio эта функция отображается в виде _OPENFILE. Visio версии 4.0 и более поздних версий принимать любого из стилей. 
  
## <a name="example"></a>Пример

 `OPENFILE("C:/MyFile.vsdx")`
  
Открывает указанный файл «MyFile.vsdx» в новом окне или активирует окно, если файл уже открыт. 
  

