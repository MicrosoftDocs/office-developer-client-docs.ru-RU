---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812444"
---
# <a name="sync"></a>SYNC

  
  
**Относится к**: Outlook 
  
Сведения о запуске синхронизации между локального хранилища и сервером. Эти сведения используются во время [синхронизации состояния](synchronize-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a>Members

 _ulFlags_
  
- [out] и [in] Битовая следующие флаги, изменяющего поведение во время синхронизации:
    
- UPS_UPLOAD_ONLY
    
  - [in] Клиент будут выполнять только отправить. Outlook возвращает только локально измененное папок.
    
- UPS_DNLOAD_ONLY
    
  - [in] Клиент будут выполнять только файл для загрузки. Outlook не должно очищать отправляемых битов для папок.
    
- UPS_THESE_FOLDERS
    
  - [in] Клиент синхронизации указанный набор папок с указанным запись идентификаторы. Этот флаг может использоваться совместно с либо **UPS_UPLOAD_ONLY** , либо **UPS_DNLOAD_ONLY** флаг. 
    
- UPS_OK
    
  - [out] Синхронизация прошла успешно. Клиент устанавливает это после отправки или завершения полной синхронизации.
    
- 
    
    > [!NOTE]
    > Несмотря на то, что клиент может отправить или полную синхронизацию (отправка и загрузка) папкам и элементам с помощью API репликации клиента указывает *ulFlags* с только в одном направлении репликации за раз, либо **UPS_UPLOAD_ONLY** или Флаг **UPS_DNLOAD_ONLY** . В случае полной синхронизации клиент не сначала отправляемых с флагом **UPS_UPLOAD_ONLY** и загрузка с флагом **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- [out] Путь к локальному хранилищу.
    
 _Reserved1_
  
- Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _Reserved2_
  
- Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 *PEL* 
  
- [in] Это список запись идентификаторы папки для синхронизации, если были установлены **UPS_THESE_FOLDERS** . В разделе mapidefs.h для определения типа **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- [in] Если были установлены **UPS_THESE_FOLDERS** это массив параметров папки для соответствующих папок в *языке выражений PerformancePoint* . Эти параметры папки используются при загрузке каждой из папок, перечисленных в *языке выражений PerformancePoint* во время [загрузки состояние папки](upload-folder-state.md). Дополнительные сведения о параметрах папки можно **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[��������� MAPI](mapi-constants.md)

