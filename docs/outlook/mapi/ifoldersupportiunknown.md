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
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808843"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Относится к**: Outlook 
  
Предоставляет сведения о поддержке папки для общего доступа.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Поставщик хранилища сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Получает сведения о поддержке папки для совместного доступа.  <br/> |
   
## <a name="remarks"></a>Замечания

Как правило Microsoft Office Outlook требуется поставщик, чтобы реализовать интерфейс, если поставщик хочет общей папки хранилища MAPI. Исключение поставщика хранилища Exchange Server, который можно совместно использовать папки не реализации этого интерфейса.
  
Клиент может запросить **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**. В случае успеха вызвать **IFolderSupport::GetSupportMask** и проверить наличие бит **FS_SUPPORTS_SHARING** должно быть задано. 
  

