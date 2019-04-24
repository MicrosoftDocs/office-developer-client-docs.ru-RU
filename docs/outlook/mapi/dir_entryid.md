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
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316676"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает свойства идентификатора записи каталога.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |код EntryID. h  <br/> |
   
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

## <a name="members"></a>Members

 **Абфлагс**
  
> Битовая маска флагов, предоставляющая информацию, описывающую объект. Дополнительные сведения можно найти в описании поля **абфлагс** структуры [EntryID](entryid.md) . 
    
 **Muid**
  
> GUID, определяющий поставщика хранилища.
    
 **Улверсион**
  
> Номер версии структуры **дир_ентрид** . Должен иметь значение КОНТАБ_ВЕРСИОН. 
    
 **Ултипе**
  
> Целое число, представляющее тип идентификатора записи каталога. Он должен иметь одно из следующих значений:
    
|**Имя**|**Описание**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Корневая папка для адресной книги MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Объект-контейнер адресной книги.  <br/> |
   
 **Муидид**
  
> Идентификатор GUID, определяющий объект logon.
    
## <a name="remarks"></a>Замечания

Структуры **дир_ентрид** и [контаб_ентрид](contab_entryid.md) идентичны, за исключением элемента **ултипе** . Содержимое элемента **ултипе** определяет, какая структура подходит для остальных полей. 
  
## <a name="see-also"></a>См. также



[CONTAB_ENTRYID](contab_entryid.md)


[Структуры MAPI](mapi-structures.md)

