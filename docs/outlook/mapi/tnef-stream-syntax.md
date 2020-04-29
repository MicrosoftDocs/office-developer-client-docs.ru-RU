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
  
В этом разделе представлено описание синтаксиса потока TNEF Бакус – Науер Like. В этом описании Нетерминальные элементы с дополнительным определением заменяются курсивом. Константы и элементы литералов выделяются полужирным шрифтом. Последовательности элементов перечисляются в одной строке по порядку. Например, элемент _Stream_ состоит из константы **TNEF_SIGNATURE**, за которыми следует _ключ_, за которым следует _объект_. Если элемент имеет несколько возможных реализаций, альтернативные варианты перечисляются в строке подряд. Например, _объект_ может состоять из _Message_Seq_, _Message_Seq_ , за которым следует _Attach_Seq_или только _Attach_Seq_.
  
 _TNEF_Stream:_
  
> _Объект_ **TNEF_SIGNATURE** _Key_
    
 _Разделе_
  
> ненулевое 16 – разрядное целое число без знака
    
Транспорты с включенной поддержкой TNEF. это значение создается перед использованием реализации TNEF для создания потока TNEF.
  
 _Объектам_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _Атттнефверсион Атттнефверсион Msg_Attribute_Seq Атттнефверсион Аттмессажекласс Атттнефверсион Аттмессажекласс Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _Атттнефверсион:_
  
> **LVL_MESSAGE атттнефверсион sizeof (ulong)** **0x00010000** CHECKSUM 
    
 _Аттмессажекласс:_
  
> **LVL_MESSAGE аттмессажекласс** _msg_class_length msg_class_ контрольной суммы 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> Атрибут **LVL_MESSAGE** Attribute — length Attribute — контрольная сумма данных 
    
Attribute-ID — это один из идентификаторов атрибутов TNEF, например **аттсубжект**. Attribute-length — это длина данных атрибута в байтах. Attribute-Data — это данные, связанные с атрибутом.
  
 _Attach_Seq:_
  
>  _Аттренддата Аттренддата Att_Attribute_Seq_
    
 _Аттренддата:_
  
> **LVL_ATTACHMENT аттренддата** **sizeof (ренддата)** ренддата контрольная сумма 
    
Ренддата — это данные, связанные с структурой **ренддата** , которые содержат информацию отображения для соответствующего вложения. Структура **ренддата** определена в формате TNEF. H файл заголовка. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> Атрибут **LVL_ATTACHMENT** Attribute — length Attribute — контрольная сумма данных 
    
Атрибуты Attribute (ID), Attribute – length и Attribute – Data имеют те же значения, что и для элемента Msg_Attribute.
  

