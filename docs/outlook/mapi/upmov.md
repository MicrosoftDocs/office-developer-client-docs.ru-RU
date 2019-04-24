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
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения для отправки перемещенных элементов. Эти сведения используются во время отправки состояния состояния [отправки](upload-delete-status-state.md) и [отправки таблицы](upload-table-state.md).
  
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
  
> возврата Флаги, необходимые для определения поведения при отправке.
    
  - UPV_ERROR
    
    - возврата Ошибка открытия папки сервера.
    
  - UPV_DIRTY
    
    - возврата Состояние отправки изменилось. Он используется клиентом для отслеживания изменений в состоянии локального хранилища.
    
  - UPV_COMMIT
    
    - возврата Состояние фиксации отправки.
    
_Сохранен_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pstmReserved_
  
>  [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pszName_
  
>  вышли Имя конечной папки. 
    
  > [!NOTE]
  > Этот элемент не поддерживает Юникод. 
  
_feid_
  
>  вышли Идентификатор записи целевой папки. 
    
_пфлд_
  
>  возврата Указатель на папку сервера. 
    
_pxicc_
  
>  возврата Указатель на интерфейс содержимого **иексчанжеимпортконтентсчанжес** , который поддерживает отправку изменений контента при использовании синхронизации добавочных изменений (ICS). Дополнительные сведения о **иексчанжеимпортконтентсчанжес** и ICS можно найти в статье [условия оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_Двресервед_
  
>  [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_Пупмовнекст_
  
>  вышли Следующий контекст перемещения. 
    
_Центмов_
  
>  возврата Количество элементов, перемещенных здесь. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [FEID](feid.md)

