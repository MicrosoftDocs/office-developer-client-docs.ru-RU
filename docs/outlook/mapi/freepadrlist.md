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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328037"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уничтожает структуру [ADRLIST](adrlist.md) и освобождает связанную память, в том числе память, выделенную для всех массивов и структур элементов. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Параметры

 _падрлист_
  
> возврата Указатель на структуру **ADRLIST** , которую необходимо уничтожить. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В рамках реализации **фрипадрлист**MAPI вызывает функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить каждую запись в структуре **ADRLIST** , прежде чем освобождать всю структуру. Таким образом, все такие записи должны следовать правилам распределения для структуры [ADRLIST](adrlist.md) , используя отдельный вызов [мапиаллокатебуффер](mapiallocatebuffer.md) для каждого массива и структуры элементов. 
  
Дополнительные сведения о выделении памяти для структур **ADRLIST** и **SRowSet** можно найти в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**�����������**|
|:-----|:-----|:-----|
|Мапиабфунктионс. cpp  <br/> |Аддонеоффаддресс  <br/> |MFCMAPI использует метод **фрипадрлист** для освобождения структуры ADRLIST, созданной для добавления к сообщению одного адреса.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

