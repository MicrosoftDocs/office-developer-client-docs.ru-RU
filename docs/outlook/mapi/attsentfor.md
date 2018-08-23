---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567477"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Атрибут **attSentFor** кодируются инвентаризации строк нужным начала до конца. Формат для **attSentFor** выглядит следующим образом: 
  
 **attSentFor**: 
  
> Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_
    
 _адрес электронной почты_
  
> Тип **:** адрес 
    
В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых. Они по-прежнему включают завершение символы null, однако. Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com». Только строка адреса объединенный тип **:** символом null.
  

