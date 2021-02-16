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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ИД записи папки контактов.
  
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
  
> Битоваяmas флагов, которая содержит сведения, описывающие объект. Дополнительные сведения см. в описании **поля abFlags** структуры [ENTRYID.](entryid.md) 
    
 **muid**
  
> GUID, идентифицирует поставщика магазина.
    
 **ulVersion**
  
> Номер версии CONTAB_ENTRYID **структуры.** Должен иметь CONTAB_VERSION. 
    
 **ulType**
  
> Integer representing the contact entry ID type. Это должно быть одно из следующих значений:
    
|**Название**|**Описание**|
|:-----|:-----|
|CONTAB_USER  <br/> |Объект пользователя, отправляющего сообщение.  <br/> |
|CONTAB_DISTLIST  <br/> |Объект списка рассылки.  <br/> |
   
 **ulIndex**
  
> Индекс в подмножество свойств электронной почты.
    
 **cbeid**
  
> Размер идентификатора записи сообщения контакта, связанного с этой записью в адресной книге контактов.
    
 **abeid**
  
> Идентификатор записи сообщения контакта, связанного с этой записью в адресной книге контактов.
    
## <a name="remarks"></a>Примечания

Адресная книга контактов — это адресная книга, которая содержит все элементы контактов в папке "Контакты" с адресом электронной почты или номером факса. Каждая запись в адресной книге контактов связана с адресом электронной почты или номером факса. Так как элемент контакта может иметь до трех адресов электронной почты и три номера факса, элемент контакта может быть представлен шестью записями в соответствующей адресной книге контактов.
  
Адресная книга контактов предназначена для поддержки пользователей, которые адресуют сообщения электронной почты контактам в папке "Контакты". Поставщик адресной книги контактов, Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013, contab32.dll.
  
Структура **CONTAB_ENTRYID** поддерживает подмножество сведений, присутствующих в основном сообщении контакта MAPI. Он определяет контактное сообщение, с которое связана определенная запись адресной книги контактов. 
  
Поля **cbeid** и **abeid** действительны, только если для поля **ulType** установлено значение CONTAB_DISTLIST или CONTAB_USER. Если для **поля ulType** установлено значение CONTAB_ROOT, CONTAB_SUBROOT или CONTAB_CONTAINER, следует [](dir_entryid.md) использовать структуру DIR_ENTRYID ulType. 
  
## <a name="see-also"></a>См. также



[DIR_ENTRYID](dir_entryid.md)


[Структуры MAPI](mapi-structures.md)

