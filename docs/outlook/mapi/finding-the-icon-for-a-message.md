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
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409155"
---
# <a name="finding-the-icon-for-a-message"></a>Поиск значка сообщения

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы найти значок, связанный с сообщением**
  
1. ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS сообщения, чтобы получить свойство **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. ВыЗовите [мапиопенформмгр](mapiopenformmgr.md) , чтобы получить указатель интерфейса **имапиформмгр** . Передайте указатель **IMAPISession** в параметр _псессион_ . 
    
3. Call [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) для получения указателя интерфейса **имапиформинфо** . 
    
4. Используйте указатель **имапиформинфо** , чтобы вызвать [IMAPIProp::](imapiprop-getprops.md) -PROPS и извлечь свойства **пр_икон** ([PidTagIcon](pidtagicon-canonical-property.md)) и/или **пр_мини_икон** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

