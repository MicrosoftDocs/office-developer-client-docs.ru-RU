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
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408840"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Атрибут **attSentFor** закодирован как подсчитываемая строка, заложенная в конец. Формат **attSentFor** следующим образом: 
  
 **attSentFor:** 
  
> адрес электронной почты с отображаемой  _именем-именем_
    
 _адрес электронной почты_
  
> **тип:** адрес 
    
В отличие от других значений длины, отображаемая длина и длина адреса являются неподписаными 16-битными значениями вместо неподписаных длинных многословий. Они по-прежнему включают прекращение null символов, однако. Строки типа и адреса в  _записи электронного_ адреса разделены буквальной двоеточием (:) символ, например "smtp:joe@nowhere.com". Только комбинированный **тип:** строка адресов не прекращается.
  

