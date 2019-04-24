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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318118"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Атрибут **аттсентфор** кодируется в виде строк, подсчитанных до конца. Формат для **аттсентфор** выглядит следующим образом: 
  
 **аттсентфор**: 
  
> Display — имя — длина отображаемого имени, адрес _электронной почты_ , длина адреса
    
 _адрес электронной почты_
  
> Тип **:** Address 
    
В отличие от других значений длины, отображаемое имя и длина адреса — это 16 – битовые значения без знака, а не длинные целые числа без знака. Тем не менее, они по-прежнему содержат завершающие символы NULL. Строки Type и Address в записи _адреса электронной почты_ разделяются с помощью литерального двоеточия (:) символ, например "SMTP:Joe@nowhere.com". Только объединенный тип **:** строка адреса завершается нулем.
  

