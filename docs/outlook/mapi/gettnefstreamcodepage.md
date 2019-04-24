---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299435"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет кодовую страницу для потока TNEF (протокол инкапсуляции формата инкапсуляции).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Параметры

 _Лпстреам_
  
> возврата Указатель на объект потока хранилища OLE **IStream** , предоставляющий источник сообщения для потока TNEF. 
    
 _Лпулкодепаже_
  
> вышли Указатель на кодовую страницу в потоке.
    
 _Лпулсубкодепаже_
  
> вышли Указатель на страницу подкода потока.
    
## <a name="return-value"></a>Возвращаемое значение

 **S_OK**
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
 **МАПИ_Е_НОТ_ЕНАУГХ_ДИСК**
  
> Произошла ошибка при чтении атрибута в потоке TNEF.
    
 **МАПИ_Е_КОРРУПТ_ДАТА**
  
> Поток не являлся потоком TNEF или возникла ошибка при чтении атрибута Аттоемкодепаже.
    
## <a name="remarks"></a>Замечания

Используйте функцию **жеттнефстреамкодепаже** для считывания атрибута **аттоемкодепаже** потока TNEF, чтобы определить кодовую страницу и страницу подкода. Если **аттоемкодепаже** не найден, **жеттнефстреамкодепаже** возвращает кодовую страницу 437 и страницу подкода 0. 
  
## <a name="see-also"></a>См. также



[Аттоемкодепаже](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

