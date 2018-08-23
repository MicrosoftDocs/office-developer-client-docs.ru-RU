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
ms.openlocfilehash: 87f5e3f159542359f614a6ab698e6f06a2faf41a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567918"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Регистрация поставщика транспорта препроцессору функция (функция, которая соответствует прототип [PreprocessMessage](preprocessmessage.md) ). 
  
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
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую идентификатор, который обрабатывает препроцессору функции. Параметр _lpMuid_ может быть NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса для сообщений, функция применяется, например, ФАКС, SMTP или X500. Параметр _lpszAdrType_ может быть NULL. 
    
 _lpszDLLName_
  
> [in] Указатель на имя библиотеки динамической компоновки (DLL), которая содержит точка входа для функции предварительной обработки.
    
 _lpszPreprocess_
  
> [in] Указатель на имя функции предварительной обработки. Параметр _lpszPreprocess_ может быть NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Указатель на имя функции, удаляющий препроцессору данные (функция, которая соответствует прототип [RemovePreprocessInfo](removepreprocessinfo.md) ). Параметр _lpszRemovePreprocessInfo_ может быть NULL. 
    
 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Функция препроцессору успешно зарегистрированы.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::RegisterPreprocessor** реализуется для поддержки объектов на транспортном поставщика. Поставщики транспорта вызов **RegisterPreprocessor** для регистрации препроцессору функции (функция, которая соответствует прототип [PreprocessMessage](preprocessmessage.md) ). Диспетчер очереди MAPI можно вызвать препроцессору функция должна быть зарегистрирована. 
  
Параметры _lpszPreprocess_, _lpszRemovePreprocessInfo_и _lpszDLLName_ должен указывать на строк, которые можно использовать в сочетании с вызова функции Win32 **GetProcAddress** , позволяя препроцессор DLL точка входа для вызова правильно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовы preprocessors относятся только к порядке поставщика транспорта. Это означает, что если обрабатывать сообщения другого поставщика транспорта раньше, чем у поставщика, препроцессору функции не вызываются для этого сообщения. Препроцессору функция будет вызываться только для сообщений, которые будет обрабатывать.
  
Вы можете использовать препроцессору функции для обработки любого из конкретного идентификатора, хранящиеся в структуре [MAPIUID](mapiuid.md) или тип адреса. При указании структуру **MAPIUID** в параметр _lpMuid_ и тип адреса с помощью параметра _lpszAdrType_ , функция будет вызываться для получателей сообщения, которые соответствуют **MAPIUID** или тип адреса. Если _lpMuid_ имеет значение NULL и _lpszAdrType_ не равно NULL, функция будет вызываться только для получателей, имеющих адрес, соответствующий тип, на который указывает _lpszAdrType_. Если _lpMuid_ не равно NULL и _lpszAdrType_ имеет значение NULL, функция будет вызываться для получателей, которые соответствуют **MAPIUID**, независимо от их типа адреса. Если оба значения NULL, функция вызывается для всех получателей сообщения.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

