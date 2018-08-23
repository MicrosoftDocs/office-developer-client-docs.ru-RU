---
title: Поиск значка сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567813"
---
# <a name="finding-the-icon-for-a-message"></a>Поиск значка сообщения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы найти значка, сопоставленного с сообщением**
  
1. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) сообщений для получения его свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Вызов [MAPIOpenFormMgr](mapiopenformmgr.md) для получения указателя интерфейса **IMAPIFormMgr** . Передайте указатель **IMAPISession** с помощью параметра _pSession_ . 
    
3. Вызов [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для получения указателя интерфейса **IMAPIFormInfo** . 
    
4. С помощью **IMAPIFormInfo** указателя Позвонить [IMAPIProp::GetProps](imapiprop-getprops.md) и получить **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) и/или свойства **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

