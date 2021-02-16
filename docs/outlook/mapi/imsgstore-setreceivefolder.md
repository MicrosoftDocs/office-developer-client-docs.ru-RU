---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434090"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устанавливает папку в качестве места назначения для входящих сообщений определенного класса сообщений.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _lpszMessageClass_
  
> [in] Указатель на класс сообщения, который должен быть связан с новой папкой получения. Если для  _параметра lpszMessageClass_ установлено значение NULL или пустая строка, **SetReceiveFolder** задает папку получения по умолчанию для хранения сообщений. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом текста в переданных строках. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строка класса сообщения имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, строка класса сообщения имеет формат ANSI.
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи папки, определяемой в качестве папки получения. Если для  _параметра lpEntryID_ задано значение NULL, **SetReceiveFolder** заменяет текущую папку получения значением по умолчанию для хранения сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка получения успешно установлена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::SetReceiveFolder** задает или изменяет папку получения для определенного класса сообщений. С **помощью SetReceiveFolder** клиент может, используя последовательные вызовы, указать разные папки получения для каждого определенного класса сообщений или указать, что входящие сообщения для нескольких классов сообщений все будут отправляться в одной папке. Например, клиент может иметь собственный класс сообщений, которые поступают в собственную папку. Приложение для факсимили может назначить одну папку, в которую поставщик магазина помещает входящие факсы, а другую папку, в которую поставщик помещает исходящую факсимилов.
  
Если во время вызова **SetReceiveFolder** возникает ошибка, параметр папки получения остается неизменным. 
  
Если **SetReceiveFolder** изменяет параметр папки получения с значением NULL для  _lpEntryID,_ указывающее на то, что папка получения по умолчанию должна быть установлена, **SetReceiveFolder** возвращает S_OK, даже если для заданного класса сообщений не существует параметров. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI использует метод **IMsgStore::SetReceiveFolder,** чтобы установить папку в качестве папки получения для определенного класса сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

