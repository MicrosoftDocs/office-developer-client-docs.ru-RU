---
title: имапимессажеситекопимессаже
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430002"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует текущее сообщение в папку.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Параметры

 _пфолдердестинатион_
  
> возврата Указатель на папку, в которую необходимо скопировать сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Эта операция не поддерживается этим сайтом сообщений.
    
## <a name="remarks"></a>Примечания

Объекты форм вызовите метод **имапимессажесите:: копимессаже** , чтобы скопировать текущее сообщение в новую папку. **Копимессаже** не изменяет сообщение, отображаемое в данный момент для пользователя, и интерфейс для нового сообщения не возвращается в форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Типичная реализация метода **копимессаже** выполняет следующие задачи: 
  
1. Создает новое сообщение для копирования текущего сообщения.
    
2. Вызывает метод [иперсистмессаже:: Save](ipersistmessage-save.md) с указателем на новое сообщение в параметре _пмессаже_ и значение false в параметре _фсамеаслоад_ . 
    
3. Вызывает метод [иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) , ПЕРЕДАВАЯ значение NULL в параметре _пмессаже_ . 
    
4. Вызывает метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для нового сообщения. 
    
Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мимапиформвиевер. cpp  <br/> |Кмимапиформвиевер:: Копимессаже  <br/> |Не реализовано.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

