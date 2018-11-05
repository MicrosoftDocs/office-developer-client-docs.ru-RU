---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393385"
---
# <a name="upmov"></a>UPMOV
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Информация для загрузки элементов, которые были перемещены. Эти сведения используются во время [загрузки удалить состояние состояния](upload-delete-status-state.md) и [Отправка состояний в таблице](upload-table-state.md).
  
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
  
> [in] Флаги для определения соответствующего поведения во время загрузки.
    
  - UPV_ERROR
    
    - [in] Ошибка при открытии папки на сервере.
    
  - UPV_DIRTY
    
    - [in] Отправить состояние изменилось. Используется клиентом для отслеживания изменений в состоянии для локального хранилища.
    
  - UPV_COMMIT
    
    - [in] Сохранить состояние передачи.
    
_Сохраняются_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pstmReserved_
  
>  [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pszName_
  
>  [out] Имя папки назначения. 
    
  > [!NOTE]
  > Этот член не поддерживает Юникод. 
  
_feid_
  
>  [out] Идентификатор записи папки назначения. 
    
_pfld_
  
>  [in] Указатель на папку сервера. 
    
_pxicc_
  
>  [in] Указатель на интерфейс **IExchangeImportContentsChanges** содержимое, которое поддерживает отправки контента изменений при использовании добавочной синхронизации изменений (ICS). Дополнительные сведения о **IExchangeImportContentsChanges** и ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.
    
_dwReserved_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pupmovNext_
  
>  [out] Далее перемещение контекста. 
    
_cEntMov_
  
>  [in] Количество элементов Переместить сюда. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [FEID](feid.md)

