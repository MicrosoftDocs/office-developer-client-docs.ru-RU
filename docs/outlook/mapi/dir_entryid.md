---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583346"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описание свойств идентификатора записи каталога.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |ENTRYID.h  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a>Элементы

 **abFlags**
  
> Битовая маска флаги, который содержит сведения, описывающие этот объект. Для получения дополнительных сведений в разделе Описание поля **abFlags** структуры [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID, идентифицирующий поставщика хранилища.
    
 **ulVersion**
  
> Номер версии структуры **DIR_ENTRYID** . Должен иметь значение CONTAB_VERSION. 
    
 **ulType**
  
> Целое число, представляющее тип идентификатор записи каталога. Оно должно быть одно из следующих значений:
    
|**Имя**|**Описание**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Корневой папки для адресную книгу MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Объект-контейнер адресной книги.  <br/> |
   
 **muidID**
  
> GUID, идентифицирующий объект вход в систему.
    
## <a name="remarks"></a>Примечания

Структур **DIR_ENTRYID** и [CONTAB_ENTRYID](contab_entryid.md) идентичны, за исключением члена **ulType** . Содержимое элемента **ulType** определяет, какие структуры подходит для остальных полях. 
  
## <a name="see-also"></a>См. также



[CONTAB_ENTRYID](contab_entryid.md)


[Структуры MAPI](mapi-structures.md)

