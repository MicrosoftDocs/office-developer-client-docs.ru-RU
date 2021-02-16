---
title: Каноническое свойство PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329276"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Каноническое свойство PidTagNormalizedSubject

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тему сообщения с удаляемой префиксом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Идентификатор:  <br/> |0x0E1D  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства вычисляются хранилищем сообщений или поставщиками транспорта из свойств **PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)и **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md)следующим образом.
  
- Если  PR_SUBJECT_PREFIX присутствует и является начальной подстрока **PR_SUBJECT,**  PR_NORMALIZED_SUBJECT и связанные свойства устанавливаются на содержимое  PR_SUBJECT с префиксом удален. 
    
- Если **PR_SUBJECT_PREFIX** присутствует, но не является начальной подстрокой **PR_SUBJECT,** **PR_SUBJECT_PREFIX** удаляется и пересчитываются из **PR_SUBJECT** с помощью следующего правила: если строка в **PR_SUBJECT** начинается с одного или трех нечислических символов, за которыми следуют двоеточие и пробел, строка вместе с двоеточием и пустым становится префиксом. Цифры, пустые символы и знаки препинания не являются допустимыми символами префикса. 
    
- Если **PR_SUBJECT_PREFIX** нет, он вычисляется из  PR_SUBJECT с помощью правила, описанного на предыдущем шаге. Затем этому свойству устанавливается содержимое PR_SUBJECT **с** удаляемым префиксом. 
    
 **Примечание** Если **PR_SUBJECT_PREFIX** пустая **строка,** PR_SUBJECT это свойство будет одинаковым. 
  
В конечном счете это свойство должно быть **частью** PR_SUBJECT после префикса. Если префикса нет, это свойство становится таким же, **как PR_SUBJECT.**
  
 **PR_SUBJECT_PREFIX** и это свойство должно быть вычислено в рамках [реализации IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Клиентские приложения не должны запросить у метода [IMAPIProp::GetProps](imapiprop-getprops.md) их значения, пока они не будут зафиксированы вызовом **IMAPIProp::SaveChanges.** 
  
Свойства темы, как правило, являются небольшими строками менее 256 символов, и поставщик хранилище сообщений не обязан поддерживать интерфейс **IStream** для связывания и встраиния объектов (OLE). Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** и использовать **IStream,** только если MAPI_E_NOT_ENOUGH_MEMORY возвращается. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
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

