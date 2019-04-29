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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о поддержке общего доступа к папке.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Поставщик хранилища сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_ифолдерсуппорт  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Получает сведения о поддержке папки для общего доступа.  <br/> |
   
## <a name="remarks"></a>Примечания

Как правило, для реализации этого интерфейса в Microsoft Office Outlook требуется поставщик хранилища MAPI, если поставщику требуется предоставить общий доступ к папке. Исключением является поставщик хранилища Exchange Server, который может предоставлять общий доступ к папкам без реализации этого интерфейса.
  
Клиент может запросить **[IMAPIFolder](imapifolderimapicontainer.md)** для **IFolderSupport**. В случае успеха вызовите метод **IFolderSupport:: GetSupportMask** и проверьте, установлен ли бит **фс_суппортс_шаринг** . 
  

