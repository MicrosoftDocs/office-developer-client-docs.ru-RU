---
title: Синтаксис потока TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812510"
---
# <a name="tnef-stream-syntax"></a>Синтаксис потока TNEF

  
  
**Относится к**: Outlook 
  
В этом разделе представлены Bakus Nauer как описание синтаксиса поток TNEF. В это описание нетерминальных элементов, которые имеют дополнительные определения, курсивом. Константы и литерал элементов — полужирным шрифтом. Последовательностей элементов перечислены в порядке на одну строку. Например элемент _потока_ состоит из константу **TNEF_SIGNATURE**, а затем _ключ_, а затем с помощью _объекта_. Если элемент содержит более одного из возможных вариантов реализации, варианты перечисляются в последовательных строк. Например, _объект_ может состоять из _Message_Seq_, _Message_Seq_ , за которым следует _Attach_Seq_или просто _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Ключ_ _Объект_
    
 _Ключ:_
  
> ненулевое 16-разрядное целое число без знака
    
Включено TNEF транспортов создать это значение перед использованием реализации TNEF для создания потока TNEF.
  
 _Объект:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof(ULONG)** контрольная сумма **0x00010000** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** контрольная сумма _msg_class_length msg_class_ 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> Контрольная сумма данных атрибутов **LVL_MESSAGE** идентификатор атрибута длина атрибутов 
    
Идентификатор атрибута — это один из идентификаторы атрибута TNEF, такие как **attSubject**. Длина атрибутов — это длина в байтах данных атрибута. Атрибут data содержит данные, связанные с помощью атрибута.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** контрольная сумма renddata **sizeof(RENDDATA)** 
    
Renddata — это данные, связанные со структурой **RENDDATA** , который содержит сведения о визуализации для соответствующих вложений. Структура **RENDDATA** определен в формате TNEF. Файл заголовка. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> Контрольная сумма данных атрибутов **LVL_ATTACHMENT** идентификатор атрибута длина атрибутов 
    
Идентификатор атрибута, длина атрибутов и данных атрибутов имеют же значения, как для элемента Msg_Attribute.
  

