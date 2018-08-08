---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808344"
---
# <a name="dntbl"></a>DNTBL
 
**Относится к**: Outlook 
  
Информация для загрузки содержимого папки с сервера во время, [Загрузите состояний в таблице](download-table-state.md), как часть полной синхронизации для содержимого для хранилища.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a>Members

_ulFlags_
  
> [in] Флаги для изменения поведения 
    
  - DNT_OK
    
    - [in] Загрузка прошла успешно. Клиент устанавливает это после загрузки информации с сервера.
    
_pstmReserved1_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pstmReserved2_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pstmReserved3_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pstmReserved4_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pxicc_
  
>  [out] Указатель на интерфейс **IExchangeImportContentsChanges** содержимое, которое поддерживает загрузки содержимого изменений. Дополнительные сведения о **IExchangeImportContentsChanges** [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
    
_pxihc_
  
>  [out] Указатель на интерфейс **IExchangeImportHierarchyChanges** иерархии, которая поддерживает загрузки изменений добавочного иерархии. Дополнительные сведения о **IExchangeImportHierarchyChanges** [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
    
_параметра pszName_
  
>  [out] Имя папки. 
    
_ftLastMod_
  
>  [out] Время последнего изменения папки. 
    
_ulRights_
  
>  [out] Значение свойства **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** папки. 
    
_feid_
  
>  [out] Идентификатор записи папки. 
    
_uintReserved_
  
>  [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_rgte_
  
> [out] Изменения для обычного (или не скрыты) и связанные (или скрытых) элементов.  *rgte [0]* — это для обычных элементов и *rgte [1]* — это для связанных элементов. Этот член заполняет Outlook во время загрузки при использовании добавочной синхронизации изменений (ICS). Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
    
_lpsrReserved_
  
>  [в] и [out] этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_boReserved_
  
>  [in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pReserved1_
  
>  [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pReserved2_
  
>  [in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
## <a name="see-also"></a>См. также

- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)  
- [��������� MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

