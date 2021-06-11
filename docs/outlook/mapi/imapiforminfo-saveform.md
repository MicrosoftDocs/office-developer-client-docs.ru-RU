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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет описание определенной формы в файле конфигурации.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameters

 _szFileName_
  
> [in] Строка, которая называет файл сообщения описания формы, в котором сохранено его описание. Это имя файла должно иметь расширение .fdm.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_EXTENDED_ERROR 
  
> Файл конфигурации не может быть написан. Чтобы получить [структуру MAPIERROR,](mapierror.md) связанную с ошибкой, позвоните по методу [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm,** вероятно, был вызван для сохранения формы в локальном контейнере форм. **SaveForm** не поддерживается в локальном контейнере форм. 
    
## <a name="remarks"></a>Примечания

Клиентские приложения называют **метод IMAPIFormInfo::SaveForm,** чтобы сохранить описание текущей формы в файле с заданным именем файла. **SaveForm** создает файл конфигурации. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете переустановить формы, выбрав их из списка сообщений описательной формы в диалоговом окне, в которое отображаются поставщики библиотек. Рекомендуемое расширение для сообщений дескриптора формы — .fdm.
  
Вызов [метода IMAPIProp::GetLastError,](imapiprop-getlasterror.md) если **SaveForm** возвращает MAPI_E_EXTENDED_ERROR, и проверьте возвращенную структуру **MAPIERROR,** чтобы определить условие, которое вызвало ошибку. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

