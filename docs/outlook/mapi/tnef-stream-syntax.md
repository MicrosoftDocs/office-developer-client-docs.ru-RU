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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе представлен Bakus-Nauer описание синтаксиса потока TNEF. В этом описании нетерминальные элементы с более подробным определением находятся в настилах. Константы и элементы литералов полужирным шрифтом. Последовательности элементов перечислены по порядку в одной строке. Например, элемент _Stream_ состоит из константы **TNEF_SIGNATURE,** за которой следует _ключ,_ за которым следует _объект._ Если элемент имеет несколько возможных реализаций, альтернативы перечислены на последовательных строках. Например, _объект_ может состоять из _Message_Seq,_ Message_Seq  с последующим Attach_Seq или просто Attach_Seq _._
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Key_ _Object_
    
 _Ключ:_
  
> 16-битное неподписаное 16-битное integer
    
Транспорты с поддержкой TNEF создают это значение перед использованием реализации TNEF для создания потока TNEF.
  
 _Объект:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE контрольной 0x00010000 attTnefVersion sizeof(ULONG)**  
    
 _attMessageClass:_
  
> **LVL_MESSAGE контрольной msg_class_length msg_class attMessageClass**  
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum 
    
Attribute-ID — это один из идентификаторов атрибутов TNEF, например **attSubject.** Длина атрибута — это длина в ветвях данных атрибута. Attribute-data — это данные, связанные с этим атрибутом.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT renddata attRenddata** **sizeof(RENDDATA)** 
    
Renddata — это данные, связанные со структурой **RENDDATA,** которая содержит сведения об отрисовки для соответствующего вложения. Структура **RENDDATA** определена в TNEF. Файл h-загона. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum 
    
Атрибуты -ID, attribute-length и attribute-data имеют то же значение, что и для Msg_Attribute элемента.
  

