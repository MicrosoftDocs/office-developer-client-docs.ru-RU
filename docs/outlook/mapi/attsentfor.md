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
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808116"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Относится к**: Outlook 
  
Атрибут **attSentFor** кодируются инвентаризации строк нужным начала до конца. Формат для **attSentFor** выглядит следующим образом: 
  
 **attSentFor**: 
  
> Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_
    
 _адрес электронной почты_
  
> Тип **:** адрес 
    
В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых. Они по-прежнему включают завершение символы null, однако. Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com». Только строка адреса объединенный тип **:** символом null.
  

