---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404899"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует функцию препроцессора транспортного поставщика (функцию, которая соответствует прототипу [PreprocessMessage).](preprocessmessage.md) 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMuid_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит идентификатор, который обрабатывает функцию препроцессора. Параметр  _lpMuid_ может быть NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса для сообщений, на которые выполняется функция, таких как ФАКС, SMTP или X500. Параметр  _lpszAdrType_ может быть NULL. 
    
 _lpszDLLName_
  
> [in] Указатель на имя библиотеки динамических ссылок (DLL), которая содержит точку входа для функции препроцессора.
    
 _lpszPreprocess_
  
> [in] Указатель на имя функции preprocessor. Параметр  _lpszPreprocess может_ быть NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Указатель на имя функции, удаляемой предпроцессорной информации (функции, соответствующей прототипу [RemovePreprocessInfo).](removepreprocessinfo.md) Параметр  _lpszRemovePreprocessInfo_ может быть NULL. 
    
 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Функция preprocessor успешно зарегистрирована.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::RegisterPreprocessor** реализован только для объектов поддержки поставщиков транспорта. Поставщики транспорта звонят **в RegisterPreprocessor** для регистрации функции препроцессора (функции, соответствующей прототипу [PreprocessMessage).](preprocessmessage.md) Перед вызовом пулера MAPI необходимо зарегистрировать функцию препроцессора. 
  
Параметры  _lpszPreprocess,_  _lpszRemovePreprocessInfo_ и  _lpszDLLName_ должны указать на строки, которые можно использовать в сочетании с вызовами к функции **Win32 GetProcAddress,** что позволяет правильно называть точку входа в DLL препроцессора. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовы к препроцессорам специфическ к заказу поставщика транспорта. Это означает, что если другой поставщик транспорта, опережая поставщика, сможет обрабатывать сообщение, функция препроцессора не будет вызвана для этого сообщения. Функция препроцессора будет вызвана только для сообщений, которые будут обрабатываться.
  
Можно написать функции препроцессора для обработки определенного идентификатора, хранимого в структуре [MAPIUID,](mapiuid.md) или типа адреса. Если в параметре _lpMuid_ указана как структура **MAPIUID,** так и тип адреса в параметре _lpszAdrType,_ ваша функция будет вызвана для получателей сообщений, которые соответствуют **типу MAPIUID** или типу адреса. Если _lpMuid_ является NULL, а _lpszAdrType_ — не NULL, ваша функция будет вызвана только для получателей с адресом, который соответствует типу, на который указывает _lpszAdrType._ Если  _lpMuid_ не является NULL и  _lpszAdrType_ является NULL, ваша функция будет вызвана для получателей, которые соответствуют **MAPIUID,** независимо от их типа адреса. Если оба являются NULL, ваша функция вызвана для всех получателей сообщения.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

