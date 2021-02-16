---
title: Каноническое свойство PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341596"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Каноническое свойство PidTagProfileHomeServerFQDN

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Включает проверку подлинности Kerberos для конфигурации профиля.
  
****

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Идентификатор:  <br/> |0x662A001F  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Установка для этого свойства доменного имени сервера каталогов пользователя позволяет напрямую установить подключение к контроллеру домена (DC), что необходимо для профиля, настроенного на использование проверки подлинности Kerberos в Microsoft Exchange Server 2007 и более ранних версиях, **путем** установки RPC_C_AUTHN_GSS_KERBEROS в **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 и Exchange Server 2013 обрабатывают вызовы адресной книги, сделанные на сервере клиентского доступа, иначе, чем вызовы в Exchange Server 2007 и более ранних версиях. Процесс DSProxy больше не используется, поэтому проверка подлинности Kerberos может быть успешной. Однако клиент по-прежнему будет связываться с сервером Exchange Server, а не напрямую с dc, что может быть не нужно: PR_PROFILE_HOME_SERVER_FQDN **этого** избежать. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для основных объектов хранения сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

