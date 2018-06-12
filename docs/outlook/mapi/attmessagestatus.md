---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808098"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Применимо к**: Outlook 
  
Отметки сообщений MAPI, сопоставляются с флаги TNEF для поддержки обратной совместимости. Все флаги объединять и кодируются в один байт. Сопоставления, как показано ниже:
  
|**Отметки сообщений MAPI**|**Флаги TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Эти параметры определены в формате TNEF. Файл заголовка.
  

