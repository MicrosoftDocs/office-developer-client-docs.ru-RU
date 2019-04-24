---
title: Имапимессажеситежетфолдер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321387"
---
# <a name="imapimessagesitegetfolder"></a>IMAPIMessageSite::GetFolder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает папку, в которой было создано или открыто текущее сообщение, если такая папка существует. Этот метод возвращает значение NULL в параметре _ппфолдер_ для внедренных сообщений, которые не хранятся непосредственно в папке. 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a>Параметры

 _Ппфолдер_
  
> вышли Указатель на указатель на возвращаемую папку.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Для сообщения не существует папки.
    
## <a name="remarks"></a>Замечания

Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: @ Folder  <br/> |MFCMAPI использует метод **имапимессажесите::** , чтобы возвратить текущий кэшированный указатель на указанную папку.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

