---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408644"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уничтожает [структуру ADRLIST](adrlist.md) и освободит связанную память, включая память, выделенную для всех массивов и структур членов. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Parameters

 _padrlist_
  
> [in] Указатель на **структуру ADRLIST,** которая должна быть уничтожена. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В рамках реализации **freePadrlist** MAPI вызывает функцию [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить каждую запись в структуре **ADRLIST** перед тем, как освободить полную структуру. Поэтому все такие записи должны следовать правилам распределения для структуры [ADRLIST,](adrlist.md) используя отдельный вызов [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого массива и структуры участников. 
  
Дополнительные сведения о деление памяти для структур **ADRLIST** и **SRowSet** см. в рубрике Управление памятью для [структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI использует метод **FreePadrlist,** чтобы освободить структуру ADRLIST, которая была построена для добавления разового адреса в сообщение.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

