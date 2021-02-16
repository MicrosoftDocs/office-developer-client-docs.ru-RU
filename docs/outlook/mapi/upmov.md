---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339188"
---
# <a name="upmov"></a>UPMOV
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения о загрузке перемещенных элементов. Эти сведения используются во время состояния [отправки и](upload-delete-status-state.md) отправки состояния [таблицы.](upload-table-state.md)
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
> [in] Флаги для определения соответствующего поведения во время отправки.
    
  - UPV_ERROR
    
    - [in] Проблема при открытии папки сервера.
    
  - UPV_DIRTY
    
    - [in] Состояние отправки изменилось. Он используется клиентом для отслеживания изменения состояния локального магазина.
    
  - UPV_COMMIT
    
    - [in] Зафиксировать состояние отправки.
    
_pReserved_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pstmReserved_
  
>  [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pszName_
  
>  [out] Имя конечной папки. 
    
  > [!NOTE]
  > Этот член не поддерживает Юникод. 
  
_feid_
  
>  [out] ИД записи конечной папки. 
    
_pfld_
  
>  [in] Указатель на папку сервера. 
    
_pxicc_
  
>  [in] Указатель на интерфейс содержимого **IExchangeImportContentsChanges,** который поддерживает отправку изменений содержимого при использовании добавонной синхронизации изменений (ICS). Дополнительные сведения об **IExchangeImportContentsChanges** и ICS см. в [критериях оценки ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)
    
_dwReserved_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pupmovNext_
  
>  [out] Контекст следующего перемещения. 
    
_cEntMov_
  
>  [in] Количество элементов, перемещенных здесь. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [FEID](feid.md)

