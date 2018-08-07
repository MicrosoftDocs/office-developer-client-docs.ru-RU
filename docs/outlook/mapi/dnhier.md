---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808345"
---
# <a name="dnhier"></a>DNHIER

**Относится к**: Outlook 
  
Сведения для загрузки иерархии с сервера во время, [Загрузите иерархия состояний](download-hierarchy-state.md), которая является частью полную иерархию синхронизации. Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS). Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
  
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

## <a name="members"></a>Members

_ulFlags_
  
>  [in] Флаги для определения соответствующего поведения во время загрузки. 
    
   - DNH_OK
    
   - [in] Загрузка прошла успешно. Клиент устанавливает это после загрузки информации с сервера.
    
_pstmReserved_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pxihc_
  
>  [out] Указатель на интерфейс **IExchangeImportHierarchyChanges** иерархии, которая поддерживает загрузки изменений добавочного иерархии. Дополнительные сведения о **IExchangeImportHierarchyChanges** [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
    
_cEntNew_
  
> [out] Число папки, добавленные в локальном хранилище. Outlook заполняет это значение во время загрузки при использовании ICS.
    
_cEntMod_
  
> [out] Число папок, которые следует изменить для локального хранилища. Outlook заполняет это значение во время загрузки при использовании ICS.
    
_cEntDel_
  
> [out] Число папок к удалению локального хранилища. Outlook заполняет это значение во время загрузки при использовании ICS.
    
## <a name="see-also"></a>См. также

- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md) 
- [��������� MAPI](mapi-constants.md)

