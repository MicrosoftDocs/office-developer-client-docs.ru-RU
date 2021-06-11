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
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423029"
---
# <a name="tnef-stream-syntax"></a>Синтаксис потока TNEF

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе Bakus-Nauer описание синтаксиса потока TNEF. В этом описании нетерминалические элементы, которые имеют дальнейшее определение, находятся в italics. Константы и буквальные элементы имеют жирный шрифт. Последовательности элементов перечислены в порядке в одной строке. Например, элемент  _Stream_ состоит из постоянной **TNEF_SIGNATURE,** а затем  _ключа_, а затем  _объекта_. Если элемент имеет несколько возможных реализаций, альтернативы перечислены в последовательной строке. Например, _объект_ может состоять из Message_Seq ,  Message_Seq с последующим Attach_Seq или просто _Attach_Seq_. 
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Key_ _Object_
    
 _Клавиша:_
  
> 16-битный неподписаный 16-битный неподписаный ряд
    
Транспорты с поддержкой TNEF создают это значение перед использованием реализации TNEF для создания потока TNEF.
  
 _Объект:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof (ULONG)** **0x00010000** checksum 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** атрибут-ID атрибут-длина атрибута-данные checksum 
    
Attribute-ID — это один из идентификаторов атрибутов TNEF, например **attSubject.** Длина атрибута — это длина в bytes данных атрибута. Атрибут-данные — это данные, связанные с атрибутом.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof (RENDDATA) renddata** checksum 
    
Renddata — это данные, связанные со структурой **RENDDATA,** которая содержит сведения о отрисовки соответствующего вложения. Структура **RENDDATA** определяется в TNEF. Файл заглавной папки H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** атрибута-ID атрибут-длина атрибут-данные checksum 
    
Атрибут-ID, длина атрибута и данные атрибута имеют те же значения, что и для элемента Msg_Attribute.
  

