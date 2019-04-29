---
title: Имапиформконтаинерресолвемессажекласс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408553"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Параметры

 _Сзмессажекласс_
  
> возврата Строка, которая указывает имя разрешаемого класса сообщений. Имена классов сообщений всегда являются строками ANSI, а не Юникодом.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих способ разрешения класса сообщения. Можно задать следующий флаг:
    
МАПИФОРМ_ЕКСАКТМАТЧ 
  
> Необходимо разрешить только строки класса сообщений с точным совпадением.
    
 _ппформинфо_
  
> вышли Указатель на указатель на возвращенный объект сведений о форме.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_НОТ_ФАУНД 
  
> Класс сообщения, переданный в параметре _сзмессажекласс_ , не соответствует классу сообщения для любой формы в контейнере формы. 
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывают метод **имапиформконтаинер:: ресолвемессажекласс** для разрешения класса сообщений в форму в контейнере формы. Объект сведений о форме, возвращенный в параметре _ппформинфо_ , предоставляет дополнительный доступ к свойствам формы с заданным классом Message. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить класс сообщения в форму, передайте имя разрешенного класса сообщения (например, `IPM.HelpDesk.Software`). Чтобы принудительно разрешить точное решение (то есть, чтобы предотвратить разрешение для базового класса класса Message), можно передать флаг МАПИФОРМ_ЕКСАКТМАТЧ в параметр _ulFlags_ . 
  
Идентификатор класса для разрешенного класса сообщения возвращается в составе объекта сведений о форме. Не следует предполагать, что идентификатор класса существует в библиотеке OLE до тех пор, пока не будет вызван метод [имапиформмгр::P репареформ](imapiformmgr-prepareform.md) или [Имапиформмгр:: креатеформ](imapiformmgr-createform.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Формконтаинердлг. cpp  <br/> |Кформконтаинердлг:: Онресолвемессажекласс  <br/> |MFCMAPI использует метод **имапиформконтаинер:: ресолвемессажекласс** для обнаружения формы, связанной с классом сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

