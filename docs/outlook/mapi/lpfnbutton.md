---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431514"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, вызываемую MAPI для активации необязательного управления кнопками в диалоговом окне адресной книги. Эта кнопка обычно является кнопкой **Details.** 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Поставщики служб  <br/> |
|Определенная функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительских окон для любых диалогов или окон эта функция отображает.
    
 _lpvContext_
  
> [in] Указатель на произвольное значение, переданного функции вызова при вызове MAPI. Это значение может представлять адрес значения для клиентского приложения. Как правило, для кода C++  _lpvContext_ представляет указатель на объект C++. 
    
 _cbEntryID_
  
> [in] Размер в bytes идентификатора записи, на который указывает параметр _lpSelection._ 
    
 _lpSelection_
  
> [in] Указатель на идентификатор записи, определяющий выбор в диалоговом окне.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Клиентские приложения называют функцию вызова на основе прототипа **LPFNBUTTON,** чтобы определить кнопку в диалоговом окне подробностей. Клиент передает указатель на функцию вызова вызовов в [метод IAddrBook::D etails.](iaddrbook-details.md) 
  
Поставщики услуг называют функцию крюка на основе прототипа **LPFNBUTTON,** чтобы определить кнопку в диалоговом окне подробностей. Поставщик передает указатель на эту функцию крючка в вызовах к методу [IMAPISupport::D etails.](imapisupport-details.md) 
  
В обоих случаях, когда диалоговое окно отображается и пользователь выбирает заданная кнопка, MAPI вызывает **LPFNBUTTON**. 
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)

