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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует функцию препроцессора поставщика транспорта (функцию, которая соответствует прототипу [PreprocessMessage).](preprocessmessage.md) 
  
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

## <a name="parameters"></a>Параметры

 _lpMuid_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит идентификатор, обрабатываемой функцией предварительной обработки. Параметр  _lpMuid может_ иметь NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса для сообщений, с которые работает функция, например ФАКС, SMTP или X500. Параметр  _lpszAdrType может_ иметь тип NULL. 
    
 _lpszDLLName_
  
> [in] Указатель на имя библиотеки динамической ссылки (DLL), которая содержит точку входа для функции препроцессора.
    
 _lpszPreprocess_
  
> [in] Указатель на имя функции препроцессора. Параметр  _lpszPreprocess может_ иметь значение NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Указатель на имя функции, которая удаляет сведения о препроцессоре (функцию, которая соответствует прототипу [RemovePreprocessInfo).](removepreprocessinfo.md) Параметр  _lpszRemovePreprocessInfo может_ иметь значение NULL. 
    
 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Функция preprocessor успешно зарегистрирована.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::RegisterPreprocessor** реализован только для объектов поддержки поставщика транспорта. Поставщики транспорта вызовите **RegisterPreprocessor** для регистрации функции препроцессора (функции, которая соответствует прототипу [PreprocessMessage).](preprocessmessage.md) Перед вызовом пулом MAPI необходимо зарегистрировать функцию preprocessor. 
  
Параметры  _lpszPreprocess,_  _lpszRemovePreprocessInfo_ и  _lpszDLLName_ должны указать на строки, которые можно использовать в сочетании с вызовами функции Win32 **GetProcAddress,** что позволяет правильно звонить точке входа DLL препроцессора. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовы к препроцессаторам специфи порядок поставщика транспорта. Это означает, что если другой поставщик транспорта перед поставщиком может обработать сообщение, функция предпроцессора не будет вызвана для этого сообщения. Функция preprocessor будет вызвана только для сообщений, которые будут обрабатываться.
  
Можно написать функции предварительной обработки для обработки определенного идентификатора, хранимого в структуре [MAPIUID](mapiuid.md) или типа адреса. Если в параметре _lpMuid_ указаны как структура **MAPIUID,** так и тип адреса в параметре _lpszAdrType,_ функция будет вызвана для получателей сообщений, которые соответствуют **типу MAPIUID** или адресу. Если _lpMuid_ имеет NULL, а _lpszAdrType_ — не NULL, функция будет вызвана только для получателей, адрес, который соответствует типу, на который указывает _lpszAdrType._ Если  _lpMuid_ не имеет NULL, а  _lpszAdrType_ — NULL, функция будет вызвана для получателей, которые соответствуют **MAPIUID,** независимо от их типа адреса. Если оба являются NULL, функция будет вызвана для всех получателей сообщения.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

