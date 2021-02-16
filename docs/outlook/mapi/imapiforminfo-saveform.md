---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428748"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сохраняет описание определенной формы в файле конфигурации.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Параметры

 _szFileName_
  
> [in] Строка, в которой имя файла сообщения описания формы, в котором сохранено ее описание. Имя файла должно иметь расширение FDM.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_EXTENDED_ERROR 
  
> Не удалось написать файл конфигурации. Чтобы получить [структуру MAPIERROR,](mapierror.md) связанную с ошибкой, вызовите метод [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) 
    
MAPI_E_NO_SUPPORT 
  
> Скорее всего, для сохранения формы в локальном контейнере формы был вызван **saveForm.** **SaveForm** не поддерживается в локальном контейнере форм. 
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывают метод **IMAPIFormInfo::SaveForm,** чтобы сохранить описание текущей формы в файле с заданным именем файла. **SaveForm** создает файл конфигурации. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно переустановить формы, выбрав их из списка сообщений дескриптора формы в диалоговом окне, которое отображают поставщики библиотеки форм. Рекомендуемое расширение для сообщений дескриптора формы — FDM.
  
Вызовите метод [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) если **SaveForm** возвращает MAPI_E_EXTENDED_ERROR, и проверьте возвращенную структуру **MAPIERROR,** чтобы определить условие, которое вызвало ошибку. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

