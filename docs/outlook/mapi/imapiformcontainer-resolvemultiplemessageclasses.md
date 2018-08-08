---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808911"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Относится к**: Outlook 
  
Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Параметры

 _pMsgClassArray_
  
> [in] Указатель на массив, содержащий имена классов сообщений для решения. Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как разрешаются классов сообщений. Можно задать следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Следует разрешить только класс строки сообщения, которые являются точное совпадение.
    
 _ppfrminfoarray_
  
> [out] Указатель на указатель на массив объектов данные формы. Если клиентское приложение с помощью параметра _pMsgClassArray_ передает значение NULL, параметр _ppfrminfoarray_ содержит объекты формы для всех форм в контейнере. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Клиентские приложения вызовите метод **IMAPIFormContainer::ResolveMultipleMessageClasses** для разрешения группы классов сообщений для форм в контейнере формы. Массив объектов формы сведений, возвращаемых в параметре _ppfrminfoarray_ дальнейшей предоставляет доступ к каждому из свойств форм. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы устранить группу классов сообщений для форм, передайте массив разрешения имен классов сообщений. Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ . 
  
Если класс сообщения не может быть разрешен в форму, для этого класса сообщений в массиве сведения формы будет возвращено значение NULL. Таким образом даже в том случае, если метод возвращает значение S_OK, не предполагают, что все классы сообщений устранены успешно. Вместо этого проверьте значения в массиве.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |Mfcmapi (en) использует метод **IMAPIFormContainer::ResolveMultipleMessageClasses** для обнаружения формы, связанный с набором классов сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

