---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430317"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Флаги сообщений MAPI соотносят с флагами TNEF, чтобы сохранить обратную совместимость. Все флаги сгруппированы и закодированы в одном byte. Сопоставления следуют следующим образом:
  
|**Флаги сообщений MAPI**|**Флаги TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Эти флаги определяются в TNEF. Файл заглавной папки H.
  

