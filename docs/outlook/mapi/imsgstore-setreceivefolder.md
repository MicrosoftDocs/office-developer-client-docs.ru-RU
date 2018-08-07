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
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809404"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Относится к**: Outlook 
  
Устанавливает папки в качестве назначения для входящих сообщений класса определенного сообщения.
  
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
  
> [in] Указатель на класс сообщений, который необходимо связать с новым получать папку. Если параметр _lpszMessageClass_ имеет значение NULL или пустая строка, **SetReceiveFolder** наборов по умолчанию получают папки для хранения сообщений. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текста в строках переданное. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> — Это строка класс сообщения в формате Юникод. Если флаг MAPI_UNICODE не установлен, — это строка класс сообщения в формате ANSI.
    
 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи папки, чтобы определить, папку получения. Если параметр _lpEntryID_ имеет значение NULL, **SetReceiveFolder** заменяет текущий получать папку с хранилище сообщений по умолчанию. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Получение папки успешно установлено.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::SetReceiveFolder** задает или изменяет папку получения для класса определенного сообщения. С помощью **SetReceiveFolder**клиента можно с помощью последовательных вызовов указать другой получать папки для каждого сообщения определенного класса или указать, что входящие сообщения для всех несколько классов сообщений перейдите к папке. Например клиент может иметь собственный класс сообщения поступают в отдельную папку. Приложение факсов можно назначить одну папку Входящие факсы помещает его поставщика хранилища и другую папку, в которой поставщик помещает исходящих факсов.
  
При возникновении ошибки во время вызова **SetReceiveFolder**, Настройка папки получения не изменяется. 
  
При изменении **SetReceiveFolder** параметр папку получения с _lpEntryID_ имеет значение NULL, указывающего на то, что необходимо задать папку получения по умолчанию, **SetReceiveFolder** возвращает значение S_OK даже в том случае, если не было отсутствуют существующие параметры для указанного Класс сообщения. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |Mfcmapi (en) использует метод **IMsgStore::SetReceiveFolder** для установки в папку в папку получения для класса определенного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

