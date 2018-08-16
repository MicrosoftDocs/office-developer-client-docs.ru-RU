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
ms.openlocfilehash: 43fd56932409861db86679eea6f1405dc4c37e62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812564"
---
# <a name="upmov"></a>UPMOV
 
**Относится к**: Outlook 
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in] Флаги для определения соответствующего поведения во время загрузки.
    
  - UPV_ERROR
    
    - [in] Ошибка при открытии папки на сервере.
    
  - UPV_DIRTY
    
    - [in] Отправить состояние изменилось. Используется клиентом для отслеживания изменений в состоянии для локального хранилища.
    
  - UPV_COMMIT
    
    - [in] Сохранить состояние передачи.
    
_Сохраняются_
  
>  [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pstmReserved_
  
>  [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_параметра pszName_
  
>  [out] Имя папки назначения. 
    
  > [!NOTE]
  > Этот член не поддерживает Юникод. 
  
_feid_
  
>  [out] Идентификатор записи папки назначения. 
    
_pfld_
  
>  [in] Указатель на папку сервера. 
    
_pxicc_
  
>  [in] Указатель на интерфейс **IExchangeImportContentsChanges** содержимое, которое поддерживает отправки контента изменений при использовании добавочной синхронизации изменений (ICS). Дополнительные сведения о **IExchangeImportContentsChanges** и ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
    
_dwReserved_
  
>  [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_pupmovNext_
  
>  [out] Далее перемещение контекста. 
    
_cEntMov_
  
>  [in] Количество элементов Переместить сюда. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [��������� MAPI](mapi-constants.md)
- [FEID](feid.md)
