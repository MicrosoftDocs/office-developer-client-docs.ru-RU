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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421237"
---
# <a name="dir_entryid"></a>DIR_ENTRYID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>"Участники"

 **абфлагс**
  
> Битовая маска флагов, предоставляющая информацию, описывающую объект. Дополнительные сведения можно найти в описании поля **абфлагс** структуры [EntryID](entryid.md) . 
    
 **Muid**
  
> GUID, определяющий поставщика хранилища.
    
 **улверсион**
  
> Номер версии структуры **DIR_ENTRYID** . Необходимо задать значение CONTAB_VERSION. 
    
 **ултипе**
  
> Целое число, представляющее тип идентификатора записи каталога. Он должен иметь одно из следующих значений:
    
|**Название**|**Описание**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Корневая папка для адресной книги MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Объект-контейнер адресной книги.  <br/> |
   
 **муидид**
  
> Идентификатор GUID, определяющий объект logon.
    
## <a name="remarks"></a>Примечания

Структуры **DIR_ENTRYID** и [CONTAB_ENTRYID](contab_entryid.md) идентичны, за исключением элемента **ултипе** . Содержимое элемента **ултипе** определяет, какая структура подходит для остальных полей. 
  
## <a name="see-also"></a>См. также



[CONTAB_ENTRYID](contab_entryid.md)


[Структуры MAPI](mapi-structures.md)

