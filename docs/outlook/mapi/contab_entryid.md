---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424086"
---
# <a name="contab_entryid"></a>CONTAB_ENTRYID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит ID записи папки контактов.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |msomapiutil.h  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a>"Участники"

 **abFlags**
  
> Битмашка флагов, которая содержит сведения, описывающие объект. Дополнительные сведения см. в описании **поля abFlags** структуры [ENTRYID.](entryid.md) 
    
 **muid**
  
> GUID, идентифицирует поставщика магазина.
    
 **ulVersion**
  
> Номер версии структуры **CONTAB_ENTRYID.** Необходимо установить CONTAB_VERSION. 
    
 **ulType**
  
> Integer, представляющий тип ID записи контакта. Это должно быть одно из следующих значений:
    
|**Имя**|**Описание**|
|:-----|:-----|
|CONTAB_USER  <br/> |Объект пользователя, отправляющего сообщение.  <br/> |
|CONTAB_DISTLIST  <br/> |Объект списка рассылки.  <br/> |
   
 **ulIndex**
  
> Индекс в подмножество свойств электронной почты.
    
 **cbeid**
  
> Размер идентификатора записи сообщения Контакт, связанного с этой записью в адресной книге Контактов.
    
 **abeid**
  
> Идентификатор записи сообщения Контакт, связанного с этой записью в адресной книге Контактов.
    
## <a name="remarks"></a>Примечания

Адресная книга контактов — это адресная книга, которая содержит все контактные элементы в папке Контакты, которые имеют либо адрес электронной почты, либо номер факса. Каждая запись в адресной книге Контактов связана либо с адресом электронной почты, либо с номером факса. Так как контактный элемент может иметь до трех адресов электронной почты и три факса, контактный элемент может быть представлен до шести записей в соответствующей адресной книге Контактов.
  
Цель адресной книги "Контакты" заключается в поддержке пользователей, обращающихся с сообщениями электронной почты к контактам в папке Contacts. Поставщик адресной книги Contacts, Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013, contab32.dll.
  
Структура **CONTAB_ENTRYID** поддерживает подмножество сведений, присутствующих в основном сообщении контакта MAPI. Он определяет сообщение Контакт, с чем связана конкретная запись адресной книги Контактов. 
  
Поля **cbeid** и **abeid** действительны только в том случае, если значение **поля ulType** CONTAB_DISTLIST или CONTAB_USER. Если значение **поля ulType** установлено для CONTAB_ROOT, CONTAB_SUBROOT или CONTAB_CONTAINER, вместо [](dir_entryid.md) DIR_ENTRYID следует использовать структуру DIR_ENTRYID. 
  
## <a name="see-also"></a>См. также



[DIR_ENTRYID](dir_entryid.md)


[Структуры MAPI](mapi-structures.md)

