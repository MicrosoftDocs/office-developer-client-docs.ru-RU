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
ms.openlocfilehash: 2af9d529cb92e1040427eba69270908dcf4a5d9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808311"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Относится к**: Outlook 
  
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

## <a name="members"></a>Members

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
|CONTAB_SUBROOT  <br/> |Подпапки, находящиеся в корневую папку объект MAPI адресной книги.  <br/> |
|CONTAB_CONTAINER  <br/> |������ ���������� �������� �����.  <br/> |
   
 **muidID**
  
> GUID, идентифицирующий объект вход в систему.
    
## <a name="remarks"></a>Замечания

Структур **DIR_ENTRYID** и [CONTAB_ENTRYID](contab_entryid.md) идентичны, за исключением члена **ulType** . Содержимое элемента **ulType** определяет, какие структуры подходит для остальных полях. 
  
## <a name="see-also"></a>См. также



[CONTAB_ENTRYID](contab_entryid.md)


[Структуры MAPI](mapi-structures.md)

