---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337004"
---
# <a name="dntbl"></a>DNTBL
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Информация для скачивания содержимого папки с сервера при [загрузке таблицы состояние](download-table-state.md) в рамках полной синхронизации содержимого хранилища.
  
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

## <a name="members"></a>Элементы

_ulFlags_
  
> [in] Отмечается для изменения поведения. 
    
  - DNT_OK
    
    - [in] Скачивание выполнено успешно. Устанавливается клиентом после скачивания информации с сервера.
    
_pstmReserved1_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pstmReserved2_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pstmReserved3_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pstmReserved4_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pxicc_
  
>  [out] Указатель для интерфейса контента **IExchangeImportContentsChanges**, который поддерживает скачивание изменений контента. Дополнительные сведения о **IExchangeImportContentsChanges** см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [out] Указатель интерфейса иерархии **IExchangeImportHierarchyChanges**, который поддерживает скачивание добавочных изменений иерархии. Дополнительные сведения о **IExchangeImportHierarchyChanges** см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [out] Имя папки. 
    
_ftLastMod_
  
>  [out] Время последнего изменения папки. 
    
_ulRights_
  
>  [out] Значение свойства ** [PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx) ** папки. 
    
_feid_
  
>  [out] Идентификатор записи папки. 
    
_uintReserved_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_rgte_
  
> [out] Изменения обычных (или не скрытых) и связанных (или скрытых) элементов.  *rgte [0]* – предназначено для обычных элементов, а *rgte [1]* – для связанных элементов. Outlook заполнит значения для данного элемента во время скачивания при использовании синхронизации добавочных изменений (ICS). Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [in]/[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_boReserved_
  
>  [in] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pReserved1_
  
>  [out]Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pReserved2_
  
>  [in] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
## <a name="see-also"></a>См. также

- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)  
- [Константы MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

