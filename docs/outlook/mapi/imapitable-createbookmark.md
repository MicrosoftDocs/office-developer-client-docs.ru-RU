---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809199"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Применимо к**: Outlook 
  
Создает закладку в текущей позиции в таблице.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parameters

 _lpbkPosition_
  
> [out] Указатель на значение возвращенные закладки 32-разрядная версия. В этом закладку более поздней версии может быть передан в вызове метода [IMAPITable::SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Запрошенная операция не может быть завершена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::CreateBookmark** отмечает позицию в таблице, создав значение, называется закладку. Закладки можно использовать для возвращения положение, определяемую средством закладки. Отмеченные положение связан с объектом в эту строку в таблице. 
  
Закладки не поддерживаются в таблицах вложений и вложений в таблице реализация **CreateBookmark** возвращать MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Из-за памяти затрат на обслуживание положения курсора с закладками Ограничьте число закладки, которые можно создать. Если отобразилась этот номер возврата MAPI_E_UNABLE_TO_COMPLETE из всех последующих вызовов **CreateBookmark**.
  
В некоторых случаях закладку указывает строку, которая больше не находится в табличном представлении. Если вызывающий объект выполняет такие закладки, переместите курсор к следующей строке видимым и остановите существует. 
  
При попытке использовать закладки, указывает невидимые строки, так как она была свернута вызывающего абонента, возвратите MAPI_W_POSITION_CHANGED после перехода к закладке. Можно изменить положение закладку в ней отображается строка, в настоящее время или после свертывания возникает в методе **SetCollapseState** . При перемещении закладки во время строку свернут, необходимо сохранить несколько в закладку, которое указывает, только когда закладки был перемещен: с момента ее последнего использования, а также если никогда не используется с момента его создания. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CreateBookmark** выделение памяти для закладки, которые он создает. Выпускает ресурсы закладки путем вызова метода [IMAPITable::FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>См. также



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

