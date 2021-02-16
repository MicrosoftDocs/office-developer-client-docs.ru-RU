---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427656"
---
# <a name="attowner"></a>attOwner

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Атрибут **attOwner** закодирован как количество строк, которые помещались в конец. Формат **attOwner:** 
  
 **attOwner**: 
  
> адрес электронной почты с отображаемой длиной отображаемого имени 
    
 _адрес электронной почты_
  
> type **:** address 
    
В отличие от других значений длины, длина отображаемого имени и длина адреса — это неподписаные 16-битные значения, а не длинные длинные. Однако они по-прежнему включают завершающие символы null. Строки типа и адреса в записи  _адреса электронной_ почты разделяются двоеточием литералов (:) символ, например "smtp:joe@nowhere.com". Только комбинированный **тип:** строка адреса завершается нулью.
  
Сопоставление свойств MAPI с атрибутом **attOwner** зависит от класса сообщения в кодируемых сообщениях. 
  

