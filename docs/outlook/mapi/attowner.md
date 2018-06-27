---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808096"
---
# <a name="attowner"></a>attOwner

  
  
**Применимо к**: Outlook 
  
Атрибут **attOwner** кодируются инвентаризации строк нужным начала до конца. Формат для **attOwner** выглядит следующим образом: 
  
 **attOwner**: 
  
> Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_
    
 _адрес электронной почты_
  
> Тип **:** адрес 
    
В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых. Они по-прежнему включают завершение символы null, однако. Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com». Только строка адреса объединенный тип **:** символом null.
  
Сопоставление свойств MAPI для атрибута **attOwner** , зависит от класса сообщений для кодирования сообщения. 
  
