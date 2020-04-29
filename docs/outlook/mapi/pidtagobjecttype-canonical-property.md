---
title: Каноническое свойство PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329227"
---
# <a name="pidtagobjecttype-canonical-property"></a>Каноническое свойство PidTagObjectType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип объекта. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_OBJECT_TYPE  <br/> |
|Идентификатор:  <br/> |0x0FFE  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Тип объекта, содержащийся в этом свойстве, соответствует основному интерфейсу, доступному для объекта, доступного через интерфейс **OpenEntry** . Обычно он получается с помощью параметра _лпулобжтипе_ , возвращаемого соответствующим методом **OpenEntry** . Когда интерфейс получается другими способами, вызовите метод [IMAPIProp::-PROPS](imapiprop-getprops.md) , чтобы получить значение этого свойства. 
  
Это свойство может иметь только одно из следующих значений:
  
MAPI_ABCONT 
  
> Объект контейнера адресной книги 
    
MAPI_ADDRBOOK 
  
> Объект адресной книги 
    
MAPI_ATTACH 
  
> Объект вложения сообщения 
    
MAPI_DISTLIST 
  
> Объект списка рассылки 
    
MAPI_FOLDER 
  
> Объект папки 
    
MAPI_FORMINFO 
  
> Объект Form 
    
MAPI_MAILUSER 
  
> Объект пользователя для обмена сообщениями 
    
MAPI_MESSAGE 
  
> Объект Message 
    
MAPI_PROFSECT 
  
> Объект раздела профиля 
    
MAPI_SESSION 
  
> Объект Session 
    
MAPI_STATUS 
  
> Объект Status 
    
MAPI_STORE 
  
> Объект хранилища сообщений
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS — NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Обрабатывает связь клиента с сервером интерфейса поставщика услуг имен (NSPI).
    
[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОАБ]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Задает форматы файлов автономной адресной книги (OAB) для кэша объектов локальной адресной книги.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСОСРЧ]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Задает свойства и операции для управления конфигурацией списка папок поиска.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

