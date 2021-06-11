---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415777"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о поддержке папки для общего доступа.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Поставщик магазина сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Получает сведения о поддержке папки для общего доступа.  <br/> |
   
## <a name="remarks"></a>Примечания

Как правило, Microsoft Office Outlook поставщик магазина MAPI должен реализовать этот интерфейс, если поставщик хочет поделиться папкой. Исключением является поставщик Exchange Server, который может обмениваться папками без реализации этого интерфейса.
  
Клиент может запрашивать **[IMAPIFolder](imapifolderimapicontainer.md)** для **IFolderSupport**. Если это удастся, **позвоните** **в IFolderSupport::GetSupportMask** и проверьте, FS_SUPPORTS_SHARING необходимо установить бит. 
  

