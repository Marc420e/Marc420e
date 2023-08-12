@pytest.mark.github_failed
def test_facebook_user_profile():
    info = [extract(parse('https://www.facebook.com/geraldine.raguindinii?mibextid=ZbWKwL')[0])]

    assert info.get('uid') == '1486042157'
    assert info.get('username') == 'anatolijsharij'
    assert info.get('fullname') == 'Анатолий Шарий'
    assert info.get('is_verified') == 'True'
    assert 'image' in info
    assert 'image_bg' in info
    assert 'all' not in info
