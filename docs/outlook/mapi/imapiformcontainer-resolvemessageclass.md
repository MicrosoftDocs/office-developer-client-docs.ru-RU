---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808906"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Относится к**: Outlook 
  
Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Параметры

 _szMessageClass_
  
> [in] Строка, имена класс сообщения, в которой необходимо разрешить. Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как устранена класс сообщения. Можно задать следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Следует разрешить только класс строки сообщения, которые являются точное совпадение.
    
 _ppforminfo_
  
> [out] Указатель на указатель на объект сведения возвращенные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданной в параметре _szMessageClass_ не соответствует класс сообщения для формы в контейнере формы. 
    
## <a name="remarks"></a>Замечания

Клиентские приложения вызовите метод **IMAPIFormContainer::ResolveMessageClass** разрешении класс сообщения в форму в контейнере формы. Объекта формы сведения, возвращаемые в параметре _ppforminfo_ дальнейшей предоставляет доступ к свойствам формы с классом данного сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы устранить класс сообщения в форму, передайте имя класса сообщений (например, `IPM.HelpDesk.Software`). Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ . 
  
Идентификатор класса для класса разрешить сообщение возвращается в составе объекта данные формы. Не следует считать, что идентификатор класса существует в библиотеке OLE до того времени, после вызова метода либо [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) , либо [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |Mfcmapi (en) использует метод **IMAPIFormContainer::ResolveMessageClass** для обнаружения формы, который связан с классом сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

