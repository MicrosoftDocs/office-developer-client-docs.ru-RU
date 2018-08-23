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
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564173"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  

