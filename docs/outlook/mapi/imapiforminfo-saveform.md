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
ms.openlocfilehash: 5e2d757fe329f9a57447723d72a859c7d82fc2b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808922"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Относится к**: Outlook 
  
Сохраняет описание определенной формы в файл конфигурации.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Параметры

 _szFileName_
  
> [in] Строка, имя файла сообщения описание формы, сохранения ее описание. Это имя файла должен иметь расширение .fdm.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_EXTENDED_ERROR 
  
> Не удалось записать файл конфигурации. Чтобы получить структура [MAPIERROR](mapierror.md) , связанный с ошибкой, вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> Возможно, **SaveForm** вызван для сохранения формы в контейнере локального формы. **SaveForm** не поддерживается для контейнера локального формы. 
    
## <a name="remarks"></a>Замечания

Клиентские приложения вызовите метод **IMAPIFormInfo::SaveForm** для сохранения описание текущей формы в файле с заданным именем файла. **SaveForm** создает файл конфигурации. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Формы можно установить, выбрав их из списка сообщений дескриптора формы в диалоговом окне, формирующих отображения поставщиков библиотеки. Рекомендуемые расширения для сообщений дескриптора формы — .fdm.
  
Вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , если **SaveForm** возвращает MAPI_E_EXTENDED_ERROR и проверьте, возвращенные структура **MAPIERROR** для определения условий, вызвавшей ошибку. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

