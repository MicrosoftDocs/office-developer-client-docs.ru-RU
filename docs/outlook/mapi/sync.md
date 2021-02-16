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
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433810"
---
# <a name="sync"></a>SYNC

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения о запуске синхронизации между локальным хранилищем и сервером. Эти сведения используются во время [синхронизации.](synchronize-state.md)
  
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

## <a name="members"></a>Элементы

 _ulFlags_
  
- [out]/[in] Битоваяmas из следующих флагов, которая изменяет поведение во время синхронизации:
    
- UPS_UPLOAD_ONLY
    
  - [in] Клиент будет выполнять только отправку. Outlook возвращает только локально измененные папки.
    
- UPS_DNLOAD_ONLY
    
  - [in] Клиент будет выполнять только скачивание. Outlook не должен очищать биты отправки для папок.
    
- UPS_THESE_FOLDERS
    
  - [in] Клиент будет синхронизировать указанный набор папок с указанными идами записей. Этот флаг можно объединить с UPS_UPLOAD_ONLY **или** **UPS_DNLOAD_ONLY** флагом. 
    
- UPS_OK
    
  - [out] Синхронизация прошла успешно. Клиент устанавливает его после отправки или завершения полной синхронизации.
    
- 
    
    > [!NOTE]
    > Несмотря на то, что клиент может либо отправить или полностью синхронизировать (загрузить, то загрузить) папки и элементы с помощью API репликации, клиент указывает *ulFlags* только с одним направлением репликации одновременно — флагом **UPS_UPLOAD_ONLY** или **UPS_DNLOAD_ONLY.** В случае полной синхронизации клиент сначала делает отправку  с флагом UPS_UPLOAD_ONLY, а затем скачивает ее с UPS_DNLOAD_ONLY **флагом.** 
  
 _pwzPath_
  
- [out] Путь к локальному магазину.
    
 _Reserved1_
  
- Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _Reserved2_
  
- Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 *pel* 
  
- [in] Это список ИД записей папок, которые необходимо синхронизировать, **UPS_THESE_FOLDERS** заданной. Определение типа **LPENTRYLIST** см. в mapidefs.h. 
    
 _pulFolderOptions_
  
- [in] Это массив параметров папок для соответствующих папок в  *pel,* **UPS_THESE_FOLDERS** заданной. Эти параметры используются при отправке каждой из папок, перечисленных в *pel,* во время состояния [папки отправки.](upload-folder-state.md) Дополнительные сведения о параметрах папок см. в **[upFLD.](upfld.md)** 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)

