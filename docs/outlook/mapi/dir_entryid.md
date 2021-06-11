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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает свойства id записи каталога.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |entryid.h  <br/> |
   
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

 **abFlags**
  
> Битмашка флагов, которая содержит сведения, описывающие объект. Дополнительные сведения см. в описании **поля abFlags** структуры [ENTRYID.](entryid.md) 
    
 **muid**
  
> GUID, идентифицирует поставщика магазина.
    
 **ulVersion**
  
> Номер версии структуры **DIR_ENTRYID.** Необходимо установить CONTAB_VERSION. 
    
 **ulType**
  
> Integer, представляющий тип ID записи каталога. Это должно быть одно из следующих значений:
    
|**Имя**|**Описание**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Корневая папка для адресной книги MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Объект-контейнер адресной книги.  <br/> |
   
 **muidID**
  
> GUID, идентифицирует объект logon.
    
## <a name="remarks"></a>Примечания

Структуры DIR_ENTRYID  [и CONTAB_ENTRYID](contab_entryid.md) идентичны, за исключением члена **ulType.** Содержимое члена **ulType** определяет, какая структура подходит для остальных полей. 
  
## <a name="see-also"></a>См. также



[CONTAB_ENTRYID](contab_entryid.md)


[Структуры MAPI](mapi-structures.md)

