        for k, v in self.iteritems():
            revdict.setdefault(v, []).append(k)
        return revdict
