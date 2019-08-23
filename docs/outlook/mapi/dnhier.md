---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337102"
---
# <a name="dnhier"></a>DNHIER

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения о скачивании иерархии с сервера во время [загрузки состояние иерархии](download-hierarchy-state.md), которая входит в состав полной иерархии синхронизации. Процесс скачивания использует синхронизацию добавочных изменений (ICS) Microsoft Exchange. Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
>  [in] Пометки для определения соответствующего поведения во время скачивания. 
    
   - DNH_OK
    
   - [in] Скачивание выполнено успешно. Устанавливается клиентом после скачивания информации с сервера.
    
_pstmReserved_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pxihc_
  
>  [out] Указатель интерфейса иерархии **IExchangeImportHierarchyChanges**, который поддерживает скачивание добавочных изменений иерархии. Дополнительные сведения о **IExchangeImportHierarchyChanges**, см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Количество папок, добавленных в локальном хранилище. Outlook заполнит это значение во время скачивания при использовании ICS.
    
_cEntMod_
  
> [out] Количество папок для изменения в локальном хранилище. Outlook заполнит это значение во время скачивания при использовании ICS.
    
_cEntDel_
  
> [out] Количество папок для удаления в локальном хранилище. Outlook заполнит это значение во время скачивания при использовании ICS.
    
## <a name="see-also"></a>См. также

- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md) 
- [Константы MAPI](mapi-constants.md)

