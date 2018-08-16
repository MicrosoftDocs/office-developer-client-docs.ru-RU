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
ms.openlocfilehash: 2c5d4ec8381d6614cc2bc92fb0a762b068a97a81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808509"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Относится к**: Outlook 
  
Удаляет структуру [ADRLIST](adrlist.md) и освобождает связанные памяти, включая объем памяти, выделенный для всех элементов массивов и структур. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Параметры

 _padrlist_
  
> [in] Указатель на структуру **ADRLIST** удалена. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Как часть его реализация **FreePadrlist**MAPI вызывает функцию [MAPIFreeBuffer](mapifreebuffer.md) для освобождения каждой записи в структуре **ADRLIST** перед очисткой полной структурой. Таким образом все записи следует правила распределения для структуры [ADRLIST](adrlist.md) , с помощью отдельного вызова [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого элемента массива и структуры. 
  
Дополнительные сведения о выделении памяти для структуры **ADRLIST** и **SRowSet** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |Mfcmapi (en) использует метод **FreePadrlist** , чтобы освободить место на структуру ADRLIST, построенный для добавления указывает адрес к сообщению.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
