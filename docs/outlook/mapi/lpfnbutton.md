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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, которую MAPI вызывает для активации дополнительного кнопки в диалоговом окне адресной книги. Эта кнопка обычно является кнопкой **"Сведения".** 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определяемая функция, реализованная в:  <br/> |Поставщики служб  <br/> |
|Определяемая функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle of the parent windows for any dialog boxes or windows this function displays.
    
 _lpvContext_
  
> [in] Указатель на произвольное значение, передав его функции вызова при вызове MAPI. Это значение может представлять адрес важности для клиентского приложения. Как правило, для кода C++  _lpvContext_ представляет указатель на объект C++. 
    
 _cbEntryID_
  
> [in] Размер идентификатора записи,на который указывает параметр  _lpSelection_ (в bytes). 
    
 _lpSelection_
  
> [in] Указатель на идентификатор записи, определяющий выделение в диалоговом окне.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызов функции вызова на основе **прототипа LPFNBUTTON** для определения кнопки в диалоговом окне сведений. Клиент передает указатель функции вызова в вызовах метода [IAddrBook::D etails.](iaddrbook-details.md) 
  
Поставщики услуг вызывать функцию обработки на основе прототипа **LPFNBUTTON,** чтобы определить кнопку в диалоговом окне сведений. Поставщик передает указатель на эту функцию обработки в вызовах метода [IMAPISupport::D etails.](imapisupport-details.md) 
  
В обоих случаях, когда отображается диалоговое окно и пользователь нажмет заданная кнопка, MAPI вызывает **LPFNBUTTON.** 
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)

