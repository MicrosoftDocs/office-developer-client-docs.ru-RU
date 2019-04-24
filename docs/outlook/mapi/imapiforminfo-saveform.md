---
title: Имапиформинфосавеформ
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321716"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет описание конкретной формы в файле конфигурации.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Параметры

 _Сзфиленаме_
  
> возврата Строка с именем файла сообщения Description формы, в котором сохраняется его описание. Это имя файла должно иметь расширение ФДМ.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_ЕКСТЕНДЕД_ЕРРОР 
  
> Не удалось записать файл конфигурации. Чтобы получить структуру [мапиеррор](mapierror.md) , связанную с ошибкой, вызовите метод [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) . 
    
МАПИ_Е_НО_СУППОРТ 
  
> **Савеформ** , вероятно, был вызван для сохранения формы в локальном контейнере форм. **Савеформ** не поддерживается в локальном контейнере форм. 
    
## <a name="remarks"></a>Замечания

Клиентские приложения вызывают метод **имапиформинфо:: савеформ** для сохранения описания текущей формы в файле с заданное именем файла. **Савеформ** создает файл конфигурации. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно переустановить формы, выбрав их в списке сообщений с дескриптором формы в диалоговом окне, в котором отображаются поставщики библиотеки форм. Рекомендуемое расширение для сообщений с дескриптором формы —. ФДМ.
  
ВыЗовите метод [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) , если **савеформ** возвращает мапи_е_екстендед_еррор, и Проверьте возвращаемую структуру **мапиеррор** , чтобы определить условие, вызвавшее ошибку. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

