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
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809656"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Относится к**: Outlook 
  
Определяет функцию обратного вызова, которая вызывает MAPI для активации элемента управления необязательно кнопка в диалоговом окне адресной книги. Эта кнопка обычно имеет кнопку **сведения** . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Функция реализован:  <br/> |Поставщики услуг  <br/> |
|Вызывается функция:  <br/> |MAPI  <br/> |
   
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
  
> [in] Дескриптор родительского windows для любого диалоговые окна или окон, эта функция отображает.
    
 _lpvContext_
  
> [in] Указатель произвольных значение передается функции обратного вызова, когда она вызывается средствами MAPI. Это значение может представлять адрес важности для клиентского приложения. Обычно для кода C++ _lpvContext_ представляет указатель на объект C++. 
    
 _cbEntryID_
  
> [in] Размер, в байтах, идентификатор записи, на который указывает параметр _lpSelection_ . 
    
 _lpSelection_
  
> [in] Указатель на идентификатор записи, определяющий выделение в диалоговом окне.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Клиентские приложения звонков на основании прототип **LPFNBUTTON** определение кнопки в диалоговом окне сведения о функции обратного вызова. Клиент передает указатель на функцию обратного вызова в вызовы метода [IAddrBook::Details](iaddrbook-details.md) . 
  
Поставщиков услуг вызова на основании прототип **LPFNBUTTON** определение кнопки в диалоговом окне сведения о функции обработчик. Поставщик передает указатель этой функции обработчика в вызовы метода [IMAPISupport::Details](imapisupport-details.md) . 
  
В обоих случаях если отображается диалоговое окно и пользователь выбирает определенный кнопка MAPI вызывает **LPFNBUTTON**. 
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)

