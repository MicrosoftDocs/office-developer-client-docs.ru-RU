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
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567155"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи из папки «Контакты».
  
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

## <a name="members"></a>Members

 **abFlags**
  
> Битовая маска флаги, который содержит сведения, описывающие этот объект. Для получения дополнительных сведений в разделе Описание поля **abFlags** структуры [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID, идентифицирующий поставщика хранилища.
    
 **ulVersion**
  
> Номер версии структуры **CONTAB_ENTRYID** . Должен иметь значение CONTAB_VERSION. 
    
 **ulType**
  
> Целое число, представляющее тип идентификатора запись контакта. Оно должно быть одно из следующих значений:
    
|**Имя**|**Описание**|
|:-----|:-----|
|CONTAB_USER  <br/> |������ ������������, ������ ����������� �����������.  <br/> |
|CONTAB_DISTLIST  <br/> |������ ������ ��������.  <br/> |
   
 **ulIndex**
  
> Индекс в набор свойств электронной почты.
    
 **cbeid**
  
> Размер идентификатор записи сообщения контакту, связанный с этой записи в адресной книге контакты.
    
 **abeid**
  
> Идентификатор записи сообщения контакту, связанного с этой записи в адресной книге контакты.
    
## <a name="remarks"></a>Замечания

В адресной книге контакты является к адресной книге, которая содержит все контактов в папке Контакты, имеющие адрес электронной почты или номер факса. Каждая запись в адресной книге контакты связан с адресом электронной почты или номер факса. Поскольку элемента контакта может иметь до трех адресов электронной почты и три факсов номера, элемента контакта можно представить в виде длиной не более шести записей в соответствующем Контакты адресной книги.
  
В адресной книге контакты предназначен для поддержки пользователей адресации сообщений электронной почты для контактов в папке «Контакты». Поставщик адресной книги контакты, Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает — contab32.dll.
  
Структура **CONTAB_ENTRYID** поддерживает подмножества данных, которые присутствуют в базовом сообщения контакту MAPI. Он определяет сообщение контакта, с которым связана записи контактов адресной книги. 
  
Поля **cbeid** и **abeid** действительны только значение поля **ulType** задано значение CONTAB_DISTLIST или CONTAB_USER. Если значение поля **ulType** CONTAB_ROOT, CONTAB_SUBROOT или CONTAB_CONTAINER, должен использоваться структуры [DIR_ENTRYID](dir_entryid.md) . 
  
## <a name="see-also"></a>См. также



[DIR_ENTRYID](dir_entryid.md)


[Структуры MAPI](mapi-structures.md)

